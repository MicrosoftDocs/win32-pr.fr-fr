---
description: 'En savoir plus sur : fonctions avec les versions Unicode (W)'
ms.assetid: 3457cfb6-3891-4e15-a4e0-53ad43adcc2d
title: Fonctions avec versions Unicode (W)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff46188554c54c19e80f80fd723500f08077a40
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469566"
---
# <a name="functions-with-unicode-w-versions"></a>Fonctions avec versions Unicode (W)

Les fonctions TAPI suivantes sont implémentées dans les versions Unicode (W) et ANSI (A). En général, l’implémentation de la version ANSI appelle la version Unicode et effectue les conversions nécessaires des paramètres ANSI et des champs de structure vers et à partir d’Unicode. le tableau suivant indique les paramètres qui sont convertis.

Les applications qui appellent explicitement la version générique (ni « W » ni suffixe « A ») d’une fonction exécutent la version ANSI, pour des compatibilité avec les versions précédentes de TAPI.

> [!Note]  
> La totalité de l’interface du fournisseur de services de téléphonie (TSPI) est au format Unicode pour la version 2,0.

 

Le tableau suivant répertorie les références aux champs de chaîne dans les structures TAPI qui se composent d’une partie des noms de champs. Par exemple, l’adresse de l’appelant dans la structure [**LINEFORWARD**](/windows/desktop/api/Tapi/ns-tapi-lineforward) est désignée par le champ **dwCallerAddressOffset** et délimitée par le champ **dwCallerAddressSize** . dans le tableau, cette chaîne est simplement identifiée comme **CallerAddress**.




| Fonction TAPI | Paramètres et champs de structure convertis en version ANSI de la fonction | 
|---------------|-----------------------------------------------------------------------|
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaddprovider"><strong>lineAddProvider</strong></a> | <em>lpszProviderName</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer"><strong>lineBlindTransfer</strong></a> | <em>lpszDestAddress</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog"><strong>lineConfigDialog</strong></a> | <em>lpszDeviceClass</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit"><strong>lineConfigDialogEdit</strong></a> | <em>lpszDeviceClass</em><blockquote>[!Note]<br />L’application doit gérer la conversion des chaînes dans <em>lpDeviceConfigIn</em> et <em>lpDeviceConfigOut</em>, si elle est directement manipulée.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedial"><strong>lineDial</strong></a> | <em>lpszDestAddress</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineforward"><strong>lineForward</strong></a> | <em>lpForwardList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineforwardlist"><strong>LINEFORWARDLIST</strong></a>)<ul><li><em>ForwardList</em> ( <a href="/windows/desktop/api/Tapi/ns-tapi-lineforward"><strong>LINEFORWARD</strong></a>)<ul><li><em>CallerAddress</em></li><li><em>DestAddress</em></li></ul></li></ul><em>lpCallParams</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallparams"><strong>LINECALLPARAMS</strong></a>)<br /><ul><li><em>OrigAddress</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li><li><em>TargetAddress</em></li><li><em>DeviceClass</em></li><li><em>CallingPartyID</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegatherdigits"><strong>lineGatherDigits</strong></a> | <em>lpsDigitslpszTerminationDigits</em><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits"><strong>lineGenerateDigits</strong></a> | <em>lpszDigits</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps"><strong>lineGetAddressCaps</strong></a> | <em>lpAddressCaps</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineaddresscaps"><strong>LINEADDRESSCAPS</strong></a>)<ul><li><em>Adresse</em></li><li><em>CompletionMsgText</em></li><li><em>DeviceClasses</em></li><li><em>CallTreatmentList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecalltreatmententry"><strong>LINECALLTREATMENTENTRY</strong></a>)</li><li><em>CallTreatmentName</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetaddressid"><strong>lineGetAddressID</strong></a> | <em>lpsAddress</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus"><strong>lineGetAddressStatus</strong></a> | <em>lpAddressStatus</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineaddressstatus"><strong>LINEADDRESSSTATUS</strong></a>)<ul><li><em>Transférer</em> ( <a href="/windows/desktop/api/Tapi/ns-tapi-lineforward"><strong>LINEFORWARD</strong></a>)</li><li><em>CallerAddress</em></li><li><em>DestAddress</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista"><strong>lineGetAgentActivityList</strong></a> | <em>lpAgentActivityList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineagentactivitylist"><strong>LINEAGENTACTIVITYLIST</strong></a>)<ul><li><em>Liste</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineagentactivityentry"><strong>LINEAGENTACTIVITYENTRY</strong></a>)</li><li><em>Nom</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa"><strong>lineGetAgentCaps</strong></a> | <em>lpAgentCaps</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineagentcaps"><strong>LINEAGENTCAPS</strong></a>)<ul><li><em>AgentHandlerInfo</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista"><strong>lineGetAgentGroupList</strong></a> | <em>lpAgentGroupListI</em>( <a href="/windows/win32/api/tapi/ns-tapi-lineagentgrouplist"><strong>LINEAGENTGROUPLIST</strong></a>)<ul><li><em>Liste</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineagentgroupentry"><strong>LINEAGENTGROUPENTRY</strong></a>)</li><li><em>Nom</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa"><strong>lineGetAgentStatus</strong></a> | <em>lpAgentStatus</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineagentstatus"><strong>LINEAGENTSTATUS</strong></a>)<ul><li><em>Activité</em></li><li><em>GroupList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineagentgroupentry"><strong>LINEAGENTGROUPENTRY</strong></a>)</li><li><em>Nom</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetapppriority"><strong>lineGetAppPriority</strong></a> | <em>lpszAppFilenamelpExtensionName</em><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo"><strong>lineGetCallInfo</strong></a> | <em>lpCallInfo</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallinfo"><strong>LINECALLINFO</strong></a>)<ul><li><em>CallerID</em></li><li><em>CallerIDName</em></li><li><em>CalledID</em></li><li><em>CalledIDName</em></li><li><em>ConnectID</em></li><li><em>ConnectedIDName</em></li><li><em>RedirectionID</em></li><li><em>RedirectionIDName</em></li><li><em>RedirectingID</em></li><li><em>RedirectingIDName</em></li><li><em>AppName</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetcountry"><strong>lineGetCountry</strong></a> | <em>lpLineCountryList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecountrylist"><strong>LINECOUNTRYLIST</strong></a>)<ul><li><em>CountryList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecountryentry"><strong>LINECOUNTRYENTRY</strong></a>)</li><li><em>CountryName</em></li><li><em>SameAreaRule</em></li><li><em>LongDistanceRule</em></li><li><em>InternationalRule</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps"><strong>lineGetDevCaps</strong></a> | <em>lpLineDevCaps</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linedevcaps"><strong>LINEDEVCAPS</strong></a>)<ul><li><em>Providerinfo retourné par</em></li><li><em>SwitchInfo</em></li><li><em>LineName</em></li><li><em>TerminalText</em></li><li><em>DeviceClasses</em></li></ul><blockquote>[!Note]<br /><em>dwStringFormat</em> est obsolète.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig"><strong>LineGetDevConfig</strong></a> | <em>lpszDeviceClass</em><blockquote>[!Note]<br />L’application doit gérer la conversion des chaînes dans <em>lpDeviceConfig</em>, si elles sont manipulées directement.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegeticon"><strong>LineGetIcon</strong></a> | <em>lpszDeviceClass</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetid"><strong>lineGetID</strong></a> | <em>lpszDeviceClass</em><blockquote>[!Note]<br />L’application doit gérer la conversion des chaînes dans <em>lpDeviceID</em>, si elles sont manipulées directement.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus"><strong>LineGetLineDevStatus</strong></a> | <em>lpLineDevStatus</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linedevstatus"><strong>LINEDEVSTATUS</strong></a>)<ul><li><em>Appinfo</em> (LINEAPPINFO)</li><li><em>MachineName</em></li><li><em>UserName</em></li><li><em>ModuleFilename</em></li><li><em>FriendlyName</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist"><strong>lineGetProviderList</strong></a> | <em>lpProviderList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineproviderlist"><strong>LINEPROVIDERLIST</strong></a>)<ul><li><em>ProviderList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-lineproviderentry"><strong>LINEPROVIDERENTRY</strong></a>)</li><li><em>ProviderFilename</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetrequest"><strong>lineGetRequest</strong></a> | <em>lpRequestBuffer</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linereqmakecall"> <strong>LINEREQMAKECALL</strong></a><ul><li><em>szDestAddress</em></li><li><em>szAppName</em></li><li><em>szCalledParty</em></li><li><em>szComment</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps"><strong>lineGetTranslateCaps</strong></a> | <em>lpTranslateCaps</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linetranslatecaps"><strong>LINETRANSLATECAPS</strong></a>)<ul><li><em>CardList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecardentry"><strong>LINECARDENTRY</strong></a>)</li><li><em>CardName</em></li><li><em>SameAreaRule</em></li><li><em>LongDistanceRule</em></li><li><em>InternationalRule</em></li><li><em>LocationList</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linelocationentry"> <strong>LINELOCATIONENTRY</strong></a></li><li><em>LocationName</em></li><li><em>CityCode</em></li><li><em>LocalAccessCode</em></li><li><em>LongDistanceAccessCode</em></li><li><em>TollPrefixList</em></li><li><em>celCallWaiting</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linehandoff"><strong>lineHandoff</strong></a> | <em>lpszFileName</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa"><strong>lineInitializeEx</strong></a> | <em>lpszFriendlyAppName</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemakecall"><strong>lineMakeCall</strong></a> | <em>lpszDestAddresslpCallParams</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallparams"><strong>LINECALLPARAMS</strong></a>)<br /><ul><li><em>OrigAddress</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li><li><em>TargetAddress</em></li><li><em>DeviceClass</em></li><li><em>CallingPartyID</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineopen"><strong>lineOpen</strong></a> | <em>lpCallParams</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallparams"><strong>LINECALLPARAMS</strong></a>)<ul><li><em>OrigAddress</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li><li><em>TargetAddress</em></li><li><em>DeviceClass</em></li><li><em>CallingPartyID</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linepark"><strong>linePark</strong></a> | <em>lpszDirAddresslpNonDirAddress</em> ( <a href="/windows/win32/api/tapi/ns-tapi-varstring"><strong>VARSTRING</strong></a>)<br /><ul><li><em>Chaîne</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linepickup"><strong>linePickup</strong></a> | <em>lpszDestAddresslpszGroupID</em><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference"><strong>linePrepareAddToConference</strong></a> | <em>lpCallParams</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallparams"><strong>LINECALLPARAMS</strong></a>)<ul><li><em>OrigAddress</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li><li><em>TargetAddress</em></li><li><em>DeviceClass</em></li><li><em>CallingPartyID</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineredirect"><strong>lineRedirect</strong></a> | <em>lpszDestAddress</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetapppriority"><strong>lineSetAppPriority</strong></a> | <em>lpszAppFilenamelpszExtensionName</em><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig"><strong>lineSetDevConfig</strong></a> | <em>lpszDeviceClass</em><blockquote>[!Note]<br />L’application doit gérer la conversion des chaînes dans <em>lpDeviceConfig</em>, si elles sont manipulées directement.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesettolllist"><strong>lineSetTollList</strong></a> | <em>lpszAddressIn</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetupconference"><strong>lineSetupConference</strong></a> | <em>lpCallParams</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallparams"><strong>LINECALLPARAMS</strong></a>)<ul><li><em>OrigAddress</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li><li><em>TargetAddress</em></li><li><em>DeviceClass</em></li><li><em>CallingPartyID</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer"><strong>lineSetupTransfer</strong></a> | <em>lpCallParams</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linecallparams"><strong>LINECALLPARAMS</strong></a>)<ul><li><em>OrigAddress</em></li><li><em>DisplayableAddress</em></li><li><em>CalledParty</em></li><li><em>Commentaire</em></li><li><em>TargetAddress</em></li><li><em>DeviceClass</em></li><li><em>CallingPartyID</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress"><strong>lineTranslateAddress</strong></a> | <em>lpszAddressInlpTranslateOutput</em> ( <a href="/windows/win32/api/tapi/ns-tapi-linetranslateoutput"><strong>LINETRANSLATEOUTPUT</strong></a>)<br /><ul><li><em>DialableString</em></li><li><em>DisplayableString</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog"><strong>lineTranslateDialog</strong></a> | <em>lpszAddressIn</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineunpark"><strong>lineUnpark</strong></a> | <em>lpszDestAddress</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog"><strong>phoneConfigDialog</strong></a> | <em>lpszDeviceClass</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo"><strong>phoneGetButtonInfo</strong></a> | <em>lpButtonInfo</em> ( <a href="/windows/win32/api/tapi/ns-tapi-phonebuttoninfo"><strong>PHONEBUTTONINFO</strong></a>)<ul><li><em>ButtonText</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps"><strong>phoneGetDevCaps</strong></a> | <em>lpPhoneCaps</em> ( <a href="/windows/win32/api/tapi/ns-tapi-phonecaps"><strong>PHONECAPS</strong></a>)<ul><li><em>Providerinfo retourné par</em></li><li><em>PhoneInfo</em></li><li><em>PhoneName</em></li><li><em>Classes de périphérique</em></li></ul><blockquote>[!Note]<br /><em>dwStringFormat</em> est obsolète.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegeticon"><strong>phoneGetIcon</strong></a> | <em>lpszDeviceClass</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetid"><strong>phoneGetID</strong></a> | <em>lpszDeviceClass</em><blockquote>[!Note]<br />L’application doit gérer la conversion des chaînes dans <em>lpDeviceID</em>, si elles sont manipulées directement.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetstatus"><strong>phoneGetStatus</strong></a> | <em>lpPhoneStatus</em> ( <a href="/windows/win32/api/tapi/ns-tapi-phonestatus"><strong>PHONESTATUS</strong></a>)<ul><li><em>OwnerName</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa"><strong>phoneInitializeEx</strong></a> | <em>lpszFriendlyAppName</em> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo"><strong>phoneSetButtonInfo</strong></a> | <em>lpButtonInfo</em> ( <a href="/windows/win32/api/tapi/ns-tapi-phonebuttoninfo"><strong>PHONEBUTTONINFO</strong></a>)<ul><li><em>ButtonTest</em></li></ul> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-tapigetlocationinfo"><strong>tapiGetLocationInfo</strong></a> | <em>lpszCountryCodelpszCityCode</em><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall"><strong>tapiRequestMakeCall</strong></a> | <em>lpszDestAddresslpszAppName</em><br /><em>lpszCalledParty</em><br /><em>lpszComment</em><br /> | 




 

 

 




