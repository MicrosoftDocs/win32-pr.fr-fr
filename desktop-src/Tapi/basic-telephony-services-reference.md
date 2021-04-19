---
description: Les fonctions de téléphonie de base sont répertoriées par catégorie dans les tableaux suivants.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Informations de référence sur les services de téléphonie de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534437"
---
# <a name="basic-telephony-services-reference"></a>Informations de référence sur les services de téléphonie de base

Les fonctions de téléphonie de base sont répertoriées par catégorie dans les tableaux suivants. Une fonction est identifiée comme [*asynchrone*](a-tapgloss.md) si elle indique la fin d’un message de réponse à l’application. Si la fonction retourne toujours son résultat à l’application immédiatement, la fonction est considérée comme [*synchrone*](s-tapgloss.md).

Voici un regroupement fonctionnel des fonctions de base de service de téléphonie :

-   [Formats d’adresse](#address-formats)
-   [Adresses](#addresses)
-   [Réponse aux appels entrants](#answering-incoming-calls)
-   [Appeler des fonctions Drop](#call-drop-functions)
-   [Appeler une manipulation de handle](#call-handle-manipulation)
-   [Contrôle des privilèges d’appel](#call-privilege-control)
-   [États d’appel et événements](#call-states-and-events)
-   [État de ligne et fonctionnalités](#line-status-and-capabilities)
-   [Négociation de version de ligne](#line-version-negotiation)
-   [Informations sur l’emplacement et le pays/la région](#location-and-countryregion-information)
-   [Appels effectués](#making-calls)
-   [Ouverture et fermeture des appareils en ligne](#opening-and-closing-line-devices)
-   [Services de destinataire de la demande](#request-recipient-services)
-   [Initialisation et arrêt de l’interface TAPI](#tapi-initialization-and-shutdown)
-   [Prise en charge de péage Saver](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a>Initialisation et arrêt de l’interface TAPI



| Fonction                                     | Description                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | Initialise l’abstraction de ligne TAPI pour une utilisation par l’application appelante. Synchronous. |
| [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | Arrête l’utilisation de l’application de l’abstraction de ligne TAPI. Synchronous.               |



 

## <a name="line-version-negotiation"></a>Négociation de version de ligne



| Fonction                                                   | Description                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | Permet à une application de négocier une version TAPI à utiliser. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>État de ligne et fonctionnalités



| Fonction                                               | Description                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | Retourne les fonctionnalités d’un périphérique de ligne donné. Synchronous.                                                                                                  |
| [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | Retourne la configuration d’un périphérique de flux multimédia. Synchronous.                                                                                                   |
| [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | Retourne l’état actuel du périphérique en ligne ouvert spécifié. Synchronous.                                                                                         |
| [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | Définit la configuration du périphérique de flux multimédia spécifié. Synchronous.                                                                                      |
| [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | Spécifie les modifications d’État pour lesquelles l’application doit être notifiée. Synchronous.                                                                      |
| [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | Retourne les paramètres de la ligne actuelle et de l’adresse de l’application. Synchronous.                                                                       |
| [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | Récupère un ID d’appareil associé à l’ouverture de ligne, à l’adresse ou à l’appel spécifié. Synchronous.                                                                  |
| [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | Permet à une application de récupérer une icône à afficher à l’utilisateur. Synchronous.                                                                                |
| [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | Fait en sorte que le fournisseur du périphérique de ligne spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés au périphérique de ligne. Synchronous. |
| [**lineConfigDialogEdit**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | Affiche une boîte de dialogue qui permet à l’utilisateur de modifier les informations de configuration d’un périphérique en ligne. Synchronous.                                                    |



 

## <a name="addresses"></a>Adresses



| Fonction                                             | Description                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | Retourne les fonctions de téléphonie d’une adresse. Synchronous.                           |
| [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | Retourne l’état actuel d’une adresse spécifiée. Synchronous.                              |
| [**lineGetAddressID**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | Récupère l’ID d’adresse d’une adresse spécifiée à l’aide d’un autre format. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Ouverture et fermeture des appareils en ligne



| Fonction                       | Description                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | Ouvre un appareil de ligne spécifié pour fournir une surveillance et/ou un contrôle ultérieurs de la ligne. Synchronous. |
| [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) | Ferme un appareil de ligne ouvert spécifié. Synchronous.                                                        |



 

## <a name="address-formats"></a>Formats d’adresse



| Fonction                                                 | Description                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | Traduit entre une adresse au format canonique et une adresse dans un format de numérotation. Synchronous. |
| [**lineSetCurrentLocation**](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | Définit l’emplacement utilisé comme contexte pour la traduction d’adresse. Synchronous.                       |
| [**lineSetTollList**](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | Manipule la liste de numéros de téléphone. Synchronous.                                                           |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | Retourne les fonctionnalités de traduction d’adresses. Synchronous.                                            |



 

## <a name="call-states-and-events"></a>États d’appel et événements



| Fonction                                         | Description                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | Retourne des informations fixes sur un appel. Synchronous.                                |
| [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | Retourne les informations d’état de l’appel complet pour l’appel spécifié. Synchronous.       |
| [**lineSetAppSpecific**](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | Définit le champ propre à l’application de la structure d’informations d’un appel. Synchronous. |



 

## <a name="making-calls"></a>Appels effectués



| Fonction                             | Description                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | Effectue un appel sortant et retourne un handle d’appel pour celui-ci. Asynchrone. |
| [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)         | Compose des adresses (parties d’une ou de plusieurs) adresses à distance. Asynchrone.         |



 

## <a name="answering-incoming-calls"></a>Réponse aux appels entrants



| Fonction                         | Description                             |
|----------------------------------|-----------------------------------------|
| [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | Répond à un appel entrant. Asynchrone. |



 

## <a name="toll-saver-support"></a>Prise en charge de péage Saver



| Fonction                                   | Description                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | Indique le nombre d’anneaux après lesquels les appels entrants doivent être traités. Synchronous.                   |
| [**lineGetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | Retourne le nombre minimal d’anneaux demandés avec [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings). Synchronous. |



 

## <a name="call-privilege-control"></a>Contrôle des privilèges d’appel



| Fonction                                             | Description                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | Définit le privilège de l’application sur le privilège spécifié. Synchronous. |



 

## <a name="call-drop-functions"></a>Appeler des fonctions Drop



| Fonction                                         | Description                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | Déconnecte un appel ou abandonne une tentative d’appel en cours. Asynchrone. |
| [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | Libère le handle d’appel spécifié. Synchronous.                       |



 

## <a name="call-handle-manipulation"></a>Appeler une manipulation de handle



| Fonction                                                   | Description                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | Transmet la propriété de l’appel et/ou modifie les privilèges d’une application en un appel. Synchronous.                                    |
| [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | Retourne des handles d’appel à des appels sur une ligne ou une adresse spécifiée pour laquelle l’application n’a pas encore de handles. Synchronous. |
| [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | Retourne une liste de handles d’appel qui font partie du même appel de conférence que l’appel spécifié en tant que paramètre. Synchronous.    |



 

## <a name="location-and-countryregion-information"></a>Informations sur l’emplacement et le pays/la région



| Fonction                                           | Description                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | Affiche une boîte de dialogue qui permet à l’utilisateur de modifier l’emplacement et d’appeler les informations de la carte. Synchronous. |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | Récupère des règles de numérotation et d’autres informations sur un pays/une région donné (e). Synchronous.              |



 

## <a name="request-recipient-services"></a>Services de destinataire de la demande

Les deux fonctions suivantes sont utilisées uniquement pour la prise en charge de la téléphonie assistée.



| Fonction                                                             | Description                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | Inscrit ou annule l’inscription de l’application en tant que destinataire de la demande pour le mode de demande spécifié. Synchronous. |
| [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | Obtient la requête suivante à partir de la bibliothèque de liens dynamiques de téléphonie. Synchronous.                                  |



 

 

 



