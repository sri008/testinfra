// // @Library('shareLibraries@main')_
// // // stage('Demo'){
// // //     steps{
// // //       script{
// // //         cronJob
// // //       }
// // //     }
// // // }
// // cronJob{}
// def config=[:]
// config.account=["ConfigSM","heloOption2"]
// pipeline {
//   agent any
//   stages {
//     stage('parameters') {
//         steps{
//             script{
//                 def userInput = [
//                     // parameters([
//                 		[
//                 			$class: 'ChoiceParameter',
//                 			choiceType: 'PT_SINGLE_SELECT',
//                 			filterLength: 0, filterable: false,
//                 			name: 'ProjectName',
//                 			script: [
//                 				$class: 'GroovyScript',
//                 				fallbackScript: 
//                 					[classpath: [],
//                 						//oldScript: '',
//                 						sandbox: false,
//                 				 		script: 'return[\'please select the project name\']'
//                 					],
//                 				script: 
//                 					[classpath: [], 
//                 					sandbox: false, 
//                 				// 	script: "return[\'${config.account[0]}\',\'${config.account[1]}\']"
//                 				    script: "return[\'${config.account[0]}\']"
//                 					]
//                 			]
//                 		],
//                 		[
//                 			$class: 'ChoiceParameter',
//                 			choiceType: 'PT_SINGLE_SELECT',
//                 			filterLength: 0, filterable: false,
//                 			name: 'ScanType',
//                 			script: [
//                 				$class: 'GroovyScript',
//                 				fallbackScript: 
//                 					[classpath: [],
//                 						sandbox: false,
//                 						script: ''
//                 					],
//                 				script: 
//                 					[classpath: [], 
//                 					sandbox: false, 
//                 					script:
//                 						'return[\'Auto\', \'Manual\']'
//                 					]
//                 			]
//                 		],
//                 		[
//                 			$class: 'CascadeChoiceParameter',
//                 			 choiceType: 'PT_SINGLE_SELECT',
//                 			name: 'Env',
//                 		    referencedParameters: 'ScanType',
//                 			script: [
//                 				$class: 'GroovyScript',
//                 				fallbackScript: 
//                 					[classpath: [],
//                 					//	oldScript: '',
//                 						sandbox: false,
//                 						script: ''
//                 					],
//                 				script: 
//                 					[classpath: [], 
//                 					sandbox: false, 
//                 					script:
//                 						'''if (ScanType == 'Auto') {
//                                           return ['dev']
//                                         }'''
//                 					]
//                 			]
//                 		],
//                 		[
//                 			$class: 'CascadeChoiceParameter',
//                 			 choiceType: 'PT_SINGLE_SELECT',
//                 			name: 'Region',
//                 		    referencedParameters: 'ScanType',
//                 			script: [
//                 				$class: 'GroovyScript',
//                 				fallbackScript: 
//                 					[classpath: [],
//                 						sandbox: false,
//                 						script: ''
//                 					],
//                 				script: 
//                 					[classpath: [], 
//                 					sandbox: false, 
//                 					script:
//                 						'''if (ScanType.equals("Auto")) {
//                                           return ["ap-south-1"]
//                                         }'''
//                 					]
//                 			]
//             		    ],
//             		    [
//                 			$class: 'CascadeChoiceParameter',
//                 			 choiceType: 'PT_SINGLE_SELECT',
//                 			name: 'Operation',
//                 		    referencedParameters: 'ScanType',
//                 			script: [
//                 				$class: 'GroovyScript',
//                 				fallbackScript: 
//                 					[classpath: [],
//                 						sandbox: false,
//                 						script: ''
//                 					],
//                 				script: 
//                 					[classpath: [], 
//                 					sandbox: false, 
//                 					script:
//                 						'''if (ScanType.equals("Auto"&& !env.ghprActualCommit)) {
//                                           return ["plan-apply", "apply", "plan-destroy", "destroy"]
//                                         }
//                                         else {
//                                             return ["plan-apply", "plan-destroy"]
//                                         }'''.stripIndent()
//                 					]
//                 			]
//             		    ]
// 	               // ])    
//                 ]
//             properties([
//                 parameters(userInput)
//                 ])
//             }
//         }
//     } 
//     stage('Build') {
//       steps {
//         // echo "${params.Environment}"
//         // echo "${params.Host}"
//         // echo "${params.ScanType}"
//         // echo "${params.Env}"
//         // echo "${params.Region}"
//         // echo "${params.Operation}"
//         echo "${params.Operation}"
//       }
//     }
//   }
// }
