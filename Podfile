# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'TestAutodeployWithPods' do
    pod 'Alamofire'
    pod 'GoogleMaps'
    pod 'CCBottomRefreshControl'
    pod 'ImageSlideshow'
    pod 'ImageSlideshow/Alamofire'
    pod 'Cosmos'
    pod 'SwiftDate'
    pod 'Simplicity'
    pod 'KeychainSwift'
    pod 'ObjectMapper'
    pod 'SwiftyBeaver'
    pod 'SideMenu'
    pod 'XLPagerTabStrip', '~> 8.0'
    pod 'NVActivityIndicatorView'
    pod 'GooglePlaces'
    pod 'UITextView+Placeholder'
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for TestAutodeployWithPods

  target 'TestAutodeployWithPodsTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'TestAutodeployWithPodsUITests' do
    inherit! :search_paths
    # Pods for testing
  end

end

post_install do |installer|
    installer.pods_project.build_configurations.each do |config|
        config.build_settings['SWIFT_VERSION'] = '4.2'
    end
    
    installer.pods_project.targets.each do |target|
        if ['Simplicity'].include? target.name
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '4.0'
            end
            else
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '4.2'
            end
        end
    end
end
