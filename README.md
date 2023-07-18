# qb-policejob
Police Job for QB-Core Framework

# Dependencies
- [ps-mdt](https://github.com/Project-Sloth/ps-mdt)
- [ps-dispatch](https://github.com/Project-Sloth/ps-dispatch)
- [ps-ui](https://github.com/Project-Sloth/ps-ui)

# Add this in qb-core/shared/items.lua
```lua
-- Spike
['spikestrip'] 			 	 	 = {['name'] = 'spikestrip', 			  			['label'] = 'Spike Strip', 				['weight'] = 200, 	    ['type'] = 'item', 		['image'] = 'spikestrip.png', 				['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,    ['combinable'] = nil,   ['description'] = 'Used to pop wheels.'},
```

# add logs in the qb-smallresources/server/logs.lua
```lua
['cuffplayer'] = '',
['evidencestash'] = '',
['pdarmory'] = '',
```

# add the image to qb-inventory/html/images

# add jobs in qb-core/shared/jobs.lua
```lua
['bcso'] = {
	label = 'BCSO',
    type = "leo",
	defaultDuty = true,
	offDutyPay = false,
	grades = {
        ['0'] = {
            name = 'Recruit',
            payment = 50
        },
		['1'] = {
            name = 'Officer',
            payment = 75
        },
		['2'] = {
            name = 'Sergeant',
            payment = 100
        },
		['3'] = {
            name = 'Lieutenant',
            payment = 125
        },
		['4'] = {
            name = 'Chief',
			isboss = true,
            payment = 150
        },
    },
},
```

# add this to qb-radialmenu/config.lua search Config.JobInteractions
```lua
["bcso"] = {
        {
            id = 'checkvehstatus',
            title = 'Check Tuning',
            icon = 'car',
            type = 'client',
            event = 'qb-tunerchip:client:TuneStatus',
            shouldClose = true
        }, {
            id = 'bcsomdt',
            title = 'BCSO MDT',
            icon = 'laptop',
            type = 'command',
            event = 'mdt',
            shouldClose = true
        }, {
            id = 'takedriverlicense',
            title = 'Revoke License',
            icon = 'id-card',
            type = 'client',
            event = 'police:client:SeizeDriverLicense',
            shouldClose = true
        }, {
            id = 'bcsointeraction',
            title = 'BCSO Actions',
            icon = 'bars',
            items = {
                {
                    id = 'escort',
                    title = 'Escort',
                    icon = 'user-friends',
                    type = 'client',
                    event = 'police:client:EscortPlayer',
                    shouldClose = true
                }, {
                    id = 'searchplayer',
                    title = 'Search',
                    icon = 'search',
                    type = 'client',
                    event = 'police:client:SearchPlayer',
                    shouldClose = true
                }, {
                    id = 'jailplayer',
                    title = 'Jail',
                    icon = 'user-lock',
                    type = 'client',
                    event = 'police:client:JailPlayer',
                    shouldClose = true
                },
            }
        }, {
            id = 'policeobjects',
            title = 'Objects',
            icon = 'road',
            items = {
                {
                    id = 'spawnpion',
                    title = 'Cone',
                    icon = 'exclamation-triangle',
                    type = 'client',
                    event = 'police:client:spawnCone',
                    shouldClose = false
                }, {
                    id = 'spawnhek',
                    title = 'Gate',
                    icon = 'torii-gate',
                    type = 'client',
                    event = 'police:client:spawnBarrier',
                    shouldClose = false
                }, {
                    id = 'spawnschotten',
                    title = 'Speed Limit Sign',
                    icon = 'sign',
                    type = 'client',
                    event = 'police:client:spawnRoadSign',
                    shouldClose = false
                }, {
                    id = 'spawntent',
                    title = 'Tent',
                    icon = 'campground',
                    type = 'client',
                    event = 'police:client:spawnTent',
                    shouldClose = false
                }, {
                    id = 'spawnverlichting',
                    title = 'Lighting',
                    icon = 'lightbulb',
                    type = 'client',
                    event = 'police:client:spawnLight',
                    shouldClose = false
                }, {
                    id = 'deleteobject',
                    title = 'Remove object',
                    icon = 'trash',
                    type = 'client',
                    event = 'police:client:deleteObject',
                    shouldClose = false
                }
            }
        }
    },
```

# Credit
* [qb-policejob](https://github.com/qbcore-framework/qb-policejob)
* [fd-spikestrips](https://github.com/ForostyDevelopment/fd-spikestrips)
