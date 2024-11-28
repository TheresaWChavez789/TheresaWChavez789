{
    "log": {
        "access": "",
        "error": "",
        "loglevel": "warning"
    },
    "inbounds": [
        {
            "tag": "socks",
            "port": 10808,
            "listen": "127.0.0.1",
            "protocol": "socks",
            "sniffing": {
                "enabled": true,
                "destOverride": [
                    "http",
                    "tls"
                ],
                "routeOnly": true
            },
            "settings": {
                "auth": "noauth",
                "udp": true,
                "allowTransparent": true
            }
        },
        {
            "tag": "http",
            "port": 10809,
            "listen": "127.0.0.1",
            "protocol": "http",
            "sniffing": {
                "enabled": true,
                "destOverride": [
                    "http",
                    "tls"
                ],
                "routeOnly": true
            },
            "settings": {
                "auth": "noauth",
                "udp": true,
                "allowTransparent": true
            }
        },
        {
            "tag": "api",
            "port": 9090,
            "listen": "127.0.0.1",
            "protocol": "dokodemo-door",
            "settings": {
                "udp": true,
                "address": "127.0.0.1",
                "allowTransparent": true
            }
        }
    ],
    "outbounds": [
        {
            "tag": "proxy",
            "protocol": "vmess",
            "settings": {
                "vnext": [
                    {
                        "address": "true.dtac.dnss.site",
                        "port": 8880,
                        "users": [
                            {
                                "id": "c777f6e0-7299-449a-8236-c0a4575a8643",
                                "alterId": 0,
                                "email": "",
                                "security": "auto",
                                "encryption": "none",
                                "flow": "tcp"
                            }
                        ]
                    }
                ]
            },
            "streamSettings": {
                "network": "ws",
                "security": "",
                "sockopt": {
                    "dialerProxy": "fragment",
                    "tcpKeepAliveIdle": 100,
                    "mark": 255,
                    "tcpNoDelay": true
                },
                "wsSettings": {
                    "path": "\/",
                    "headers": {
                        "Host": "www.opensignal.com.v2ray.tikvpn.shop"
                    }
                }
            },
            "mux": {
                "enabled": true,
                "concurrency": 15,
                "xudpConcurrency": 15,
                "xudpProxyUDP443": "reject"
            }
        },
        {
            "tag": "fragment",
            "protocol": "freedom",
            "settings": {
                "domainStrategy": "AsIs",
                "fragment": {
                    "packets": "tlshello",
                    "length": "10-20",
                    "interval": "10-30"
                }
            },
            "streamSettings": {
                "sockopt": {
                    "dialerProxy": "direct",
                    "tcpNoDelay": true,
                    "tcpKeepAliveIdle": 100
                }
            }
        },
        {
            "tag": "direct",
            "protocol": "freedom",
            "settings": {}
        },
        {
            "tag": "block",
            "protocol": "blackhole",
            "settings": {
                "response": {
                    "type": "http"
                }
            }
        }
    ],
  "project_info": {
    "project_id": "mockproject-1234",
    "project_number": "123456789000",
    "name": "FirebaseQuickstarts",
    "firebase_url": "https://mockproject-1234.firebaseio.com"
  },
  "client": [
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.samples.quickstart.admobexample",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.samples.quickstart.admobexample",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.samples.quickstart.admobexample",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.firebase.quickstart.analytics",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.firebase.quickstart.analytics",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.firebase.quickstart.analytics",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.samples.quickstart.appindexing",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.samples.quickstart.appindexing",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.samples.quickstart.appindexing",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.firebase.quickstart.auth",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.firebase.quickstart.auth",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.firebase.quickstart.auth",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.samples.quickstart.config",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.samples.quickstart.config",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.samples.quickstart.config",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.samples.quickstart.crash",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.samples.quickstart.crash",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.samples.quickstart.crash",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.firebase.quickstart.database",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.firebase.quickstart.database",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.firebase.quickstart.database",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.firebase.quickstart.deeplinks",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.firebase.quickstart.deeplinks",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.firebase.quickstart.deeplinks",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.firebase.quickstart.invites",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.firebase.quickstart.invites",
          "certificate_hash": []
        }
      },
      "oauth_client": [
        {
          "client_id": "123456789000-hjugbg6ud799v4c49dim8ce2usclthar.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.google.firebase.quickstart.invites",
            "certificate_hash": "4C20644DE36B8F89D25650C7D1FF9FBAE650FDF7"
          }
        },
        {
          "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzbSzCn1N6LWIe6wthYyrgUUSAlUsdqMb-wvTo"
        }
      ],
      "services": {
        "analytics_service": {
          "status": 1
        },
        "cloud_messaging_service": {
          "status": 2,
          "apns_config": []
        },
        "appinvite_service": {
          "status": 2,
          "other_platform_oauth_client": [
            {
              "client_id": "123456789000-e4uksm38sne0bqrj6uvkbo4oiu4hvigl.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        },
        "google_signin_service": {
          "status": 2
        },
        "ads_service": {
          "status": 2,
          "test_banner_ad_unit_id": "ca-app-pub-3940256099942544/6300978111",
          "test_interstitial_ad_unit_id": "ca-app-pub-3940256099942544/1033173712"
        }
      }
    },
    {
      "client_info": {
        "mobilesdk_app_id": "1:123456789000:android:f1bf012572b04063",
        "client_id": "android:com.google.firebase.example.fireeats",
        "client_type": 1,
        "android_client_info": {
          "package_name": "com.google.firebase.examp
