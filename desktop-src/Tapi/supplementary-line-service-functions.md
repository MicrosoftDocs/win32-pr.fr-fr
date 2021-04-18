---
description: Les fonctions de service en ligne supplémentaires sont répertoriées par catégorie dans les rubriques suivantes.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Fonctions de service en ligne supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533882"
---
# <a name="supplementary-line-service-functions"></a>Fonctions de service en ligne supplémentaires

Les fonctions de service en ligne supplémentaires sont répertoriées par catégorie dans les rubriques suivantes. Une fonction est identifiée comme [*asynchrone*](a-tapgloss.md) si elle indique la fin d’un message de réponse à l’application. Si la fonction retourne toujours son résultat à l’application immédiatement, la fonction est considérée comme [*synchrone*](s-tapgloss.md).

Voici un regroupement fonctionnel des fonctions de service en ligne supplémentaires :

-   [Agents](#agents)
-   [Priorité de l’application](#application-priority)
-   [Taux et mode de support](#bearer-mode-and-rate)
-   [Appeler accepter et rediriger](#call-accept-and-redirect)
-   [Fin de l’appel](#call-completion)
-   [Appeler une conférence](#call-conference)
-   [Transfert d’appels](#call-forwarding)
-   [Recevoir un appel](#call-hold)
-   [Parc d’appels](#call-park)
-   [Prélèvement d’appels](#call-pickup)
-   [Appel refusé](#call-reject)
-   [Transfert d’appels](#call-transfer)
-   [Chiffrer la surveillance et la collecte](#digit-monitoring-and-gathering)
-   [Génération de chiffres et de tonalités inbande](#generating-inband-digits-and-tones)
-   [Appels effectués](basic-telephony-services-reference.md)
-   [Contrôle multimédia](#media-control)
-   [Surveillance des médias](#media-monitoring)
-   [Proxies](#proxies)
-   [Qualité de service](#quality-of-service)
-   [Envoi d’informations au tiers distant](#sending-information-to-remote-party)
-   [Gestion des fournisseurs de services](#service-provider-management)
-   [Définition d’un terminal pour les conversations sur téléphone](#setting-a-terminal-for-phone-conversations)
-   [Analyse des tons](#tone-monitoring)

Il existe également [diverses](#miscellaneous) fonctions de service de ligne supplémentaires.

## <a name="bearer-mode-and-rate"></a>Taux et mode de support



| Fonction                                       | Description                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Demande une modification des paramètres d’appel d’un appel existant. Synchronous. |



 

## <a name="media-monitoring"></a>Surveillance des médias



| Fonction                                     | Description                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Active ou désactive la notification en mode Media sur un appel spécifié. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Chiffrer la surveillance et la collecte



| Fonction                                       | Description                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Active ou désactive la notification de détection de chiffres sur un appel spécifié. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Exécute la collecte mise en mémoire tampon des chiffres sur un appel. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Analyse des tons



| Fonction                                     | Description                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Spécifie les tonalités à détecter sur un appel spécifié. Synchronous. |



 

## <a name="media-control"></a>Contrôle multimédia



| Fonction                                           | Description                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Définit le flux multimédia d’un appel pour le contrôle multimédia. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Définit le (s) mode (s) de support de l’appel spécifié dans sa structure [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) . Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Génération de chiffres et de tonalités inbande



| Fonction                                         | Description                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Génère des chiffres inbandes sur un appel. Synchronous.               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Génère un ensemble donné de tonalités inbande sur un appel. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Appeler accepter et rediriger



| Fonction                             | Description                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Accepte un appel proposé et démarre l’alerte à la fois de l’appelant (rappel) et du tiers appelé tiers (sonnerie). Asynchrone. |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Redirige un appel d’offre vers une autre adresse. Asynchrone.                                              |



 

## <a name="call-reject"></a>Appel refusé



| Fonction                     | Description                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Déconnecte un appel ou abandonne une tentative d’appel en cours. Asynchrone. |



 

## <a name="call-hold"></a>Recevoir un appel



| Fonction                         | Description                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Place l’appel spécifié sur un blocage matériel. Asynchrone. |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Récupère un appel détenu. Asynchrone.                  |



 

## <a name="securing-calls"></a>Sécurisation des appels



| Fonction                                 | Description                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Sécurise un appel existant contre les interférences par d’autres événements tels que les bips d’attente d’appels sur les connexions de données. Asynchrone. |



 

## <a name="call-transfer"></a>Transfert d’appels



| Fonction                                             | Description                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Prépare un appel spécifié pour le transfert vers une autre adresse. Asynchrone.                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Transfère un appel qui a été configuré pour le transfert vers un autre appel ou entre une conférence triple. Asynchrone. |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Transfère un appel à un tiers. Asynchrone.                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Permute l’appel actif avec l’appel actuellement sur la suspension de la consultation. Asynchrone.                              |



 

## <a name="call-conference"></a>Appeler une conférence



| Fonction                                                         | Description                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Prépare un appel donné pour l’ajout d’un tiers. Asynchrone.                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Prépare l’ajout d’un tiers à un appel de conférence existant en plaçant l’appel de conférence dans un état de suspension et en créant un appel de consultation qui peut être ajouté ultérieurement à l’appel de conférence. Asynchrone. |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Ajoute un appel de consultation à un appel de conférence existant. Asynchrone.                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Supprime un tiers d’un appel de conférence. Asynchrone.                                                                                                                                                |



 

## <a name="call-park"></a>Parc d’appels



| Fonction                         | Description                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Traite un appel donné à une autre adresse. Asynchrone. |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Récupère un appel parqué. Asynchrone.               |



 

## <a name="call-forwarding"></a>Transfert d’appels



| Fonction                           | Description                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Définit ou annule les demandes de transfert d’appel. Asynchrone. |



 

## <a name="call-pickup"></a>Prélèvement d’appels



| Fonction                         | Description                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Récupère une alerte d’appel à une adresse de destination spécifiée et retourne un descripteur d’appel pour l’appel prélevé ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut également être utilisé pour l’appel en attente). Asynchrone. |



 

## <a name="sending-information-to-remote-party"></a>Envoi d’informations au tiers distant



| Fonction                                                   | Description                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Libère les informations de l’utilisateur, en permettant au système de remplacer ce stockage par de nouvelles informations. Asynchrone. |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Envoie des informations utilisateur-utilisateur au tiers distant sur l’appel spécifié. Asynchrone.                                |



 

## <a name="call-completion"></a>Fin de l’appel



| Fonction                                         | Description                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Place une demande d’achèvement d’appel. Asynchrone.  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Annule une demande d’achèvement d’appel. Asynchrone. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Définition d’un terminal pour les conversations sur téléphone



| Fonction                                   | Description                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Spécifie l’appareil Terminal Server vers lequel les événements de ligne, d’adresse ou de flux de média d’appel sont routés. Asynchrone. |



 

## <a name="application-priority"></a>Priorité de l’application



| Fonction                                         | Description                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Récupère des informations sur la priorité de la téléphonie et/ou assistée pour une application. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Définit le transfert et/ou la priorité de téléphonie assistée pour une application. Synchronous.              |



 

## <a name="service-provider-management"></a>Gestion des fournisseurs de services



| Fonction                                           | Description                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Installe un fournisseur de services de téléphonie. Synchronous.                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Affiche la boîte de dialogue de configuration d’un fournisseur de services. Synchronous. |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Supprime un fournisseur de services de téléphonie existant. Synchronous.          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Récupère la liste des fournisseurs de services installés. Synchronous.         |



 

## <a name="agents"></a>Agents



| Fonction                                                     | Description                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Permet à l’application d’accéder aux fonctions spécifiques du gestionnaire d’agents associées à l’adresse. Asynchrone. |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Obtient la liste des activités à partir desquelles une application sélectionne les fonctions qu’un agent exécute. Asynchrone.                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Obtient les fonctionnalités liées à l’agent prises en charge sur le périphérique de ligne spécifié. Asynchrone.                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Obtient la liste des groupes d’agents dans lesquels un agent peut se connecter sur le serveur de distribution d’appels automatique. Asynchrone.                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Obtient l’état relatif à l’agent sur l’adresse spécifiée. Asynchrone.                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Définit le code d’activité de l’agent associé à une adresse particulière. Asynchrone.                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Définit les groupes d’agents sur lesquels l’agent est connecté à une adresse particulière. Asynchrone.                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Définit l’état de l’agent associé à une adresse particulière. Asynchrone.                                                                |



 

## <a name="proxies"></a>Proxies



| Fonction                                       | Description                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Utilisé par un gestionnaire de demandes de proxy inscrit pour générer des messages TAPI. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Indique la fin d’une demande de proxy par un gestionnaire de proxy inscrit. Synchronous. |



 

## <a name="quality-of-service"></a>Qualité de service



| Fonction                                                           | Description                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Demande une modification des paramètres de qualité de service pour un appel existant. Asynchrone. |



 

## <a name="miscellaneous"></a>Divers



| Fonction                                             | Description                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Définit le membre **CallData** de la structure [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) . Asynchrone. |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Définit les sons que l’utilisateur entend lorsqu’un appel n’est pas répondu ou qu’il est en attente. Asynchrone.               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Définit l’état de l’appareil de ligne. Asynchrone.                                                            |



 

 

 



