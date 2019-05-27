platform :ios, '11.0'

target 'ReMember' do
    pod 'BMSCore', '~> 2.0'

    pod 'SwiftCloudant', :git => 'https://github.com/cloudant/swift-cloudant.git'
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for ReMember

    pod 'RxSwift',    '~> 4.0'
    pod 'RxCocoa',    '~> 4.0'
    pod 'SwiftyJSON'
    pod 'PKHUD',      '~> 5.0'
    pod 'IBMWatsonVisualRecognitionV3', '~> 1.3.1'

    post_install do |installer|
        installer.pods_project.targets.each do |target|
            if ['SwiftCloudant'].include? target.name
                target.build_configurations.each do |config|
                    config.build_settings['SWIFT_VERSION'] = '3.2'
                end
            end
        end
    end

  target 'ReMemberTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'ReMemberUITests' do
    inherit! :search_paths
    # Pods for testing
  end

end
