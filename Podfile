platform :ios, '8.0'

use_frameworks!
inhibit_all_warnings!

def pods
  # Commons
  pod 'CocoaLumberjack/Swift'
  pod 'HockeySDK'
  # Core
  pod 'Firebase/Core'
  pod 'Firebase/Auth'
  pod 'Firebase/Messaging'
  # Components
  pod 'ActiveLabel', :git => 'https://github.com/optonaut/ActiveLabel.swift', :commit => '3f869d1'
  pod 'PhoneNumberKit', :git => 'https://github.com/marmelroy/PhoneNumberKit.git', :branch => 'master'
  pod 'SVProgressHUD'
  pod 'JSQWebViewController'
  # Utils
  pod 'Localize-Swift'
end

target 'Bitrise-iOS-Test' do
  pods
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['SWIFT_VERSION'] = '4.0'
        end
    end
end
