---
title: WNet, fonctions
description: Les fonctions de réseau Windows fournissent des informations et des utilitaires pour la gestion des ressources réseau.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623de7adfdb57e21f01bff8b9647d6d2d175bd63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199335"
---
# <a name="wnet-functions"></a>WNet, fonctions

Les fonctions de réseau Windows fournissent des informations et des utilitaires pour la gestion des ressources réseau. Les fonctions de mise en réseau Windows peuvent être regroupées comme suit :

-   [Fonctions de connexion](#connection-functions)
-   [Fonctions d’énumération](#enumeration-functions)
-   [Fonctions d'information](#information-functions)
-   [Fonctions utilisateur](#user-functions)

## <a name="connection-functions"></a>Fonctions de connexion

Appelez les fonctions de connexion WNet suivantes pour connecter un appareil local à une ressource réseau et pour annuler des connexions réseau.



| Fonction                                                                     | Description                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Retourne des informations sur les performances attendues d’une connexion à une ressource réseau.                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Connecte un appareil local à une ressource réseau. (Fourni pour la compatibilité avec les versions 16 bits de Windows.)                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Connecte un appareil local à une ressource réseau.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Connecte un appareil local à une ressource réseau. Cette fonction comprend un paramètre supplémentaire que la fonction **WNetAddConnection2** , un handle vers une fenêtre que le fournisseur réseau peut utiliser comme fenêtre propriétaire pour les boîtes de dialogue. |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Annule une connexion réseau. (Fourni pour la compatibilité avec les versions 16 bits de Windows.)                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Annule une connexion réseau, ce qui permet de mettre à jour le profil utilisateur avec des informations sur les connexions persistantes.                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Démarre une boîte de dialogue d’exploration générale pour la connexion aux ressources réseau.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Démarre une boîte de dialogue d’exploration générale pour la connexion aux ressources réseau, à l’aide d’une structure [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Démarre une boîte de dialogue d’exploration générale pour la déconnexion des ressources réseau.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Démarre une boîte de dialogue d’exploration générale pour la déconnexion des ressources réseau, à l’aide d’une structure [**DISCDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) .                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Récupère le nom de la ressource réseau associée à un appareil local.                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Lorsqu’il s’agit d’un chemin d’accès basé sur un lecteur pour une ressource réseau, retourne une forme plus universelle du nom.                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Restaure la connexion à une ressource réseau, en invitant l’utilisateur, le cas échéant, à entrer un nom et un mot de passe.                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Connecte un appareil local à une ressource réseau ; sélectionne automatiquement un appareil local inutilisé pour rediriger vers la ressource réseau.                                                                                               |



 

> [!Note]  
> Les fonctions [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) et [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) sont prises en charge pour la compatibilité avec Windows pour les groupes de travail. Toutefois, les nouvelles applications doivent utiliser [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), et [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

 

## <a name="enumeration-functions"></a>Fonctions d’énumération

Appelez les fonctions WNet suivantes pour énumérer les ressources réseau.



| Fonction                                     | Description                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Met fin à une énumération des ressources réseau.                                                    |
| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Poursuit une énumération des ressources réseau démarrées par la fonction **WNetOpenEnum** . |
| [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Démarre une énumération des ressources réseau.                                             |



 

## <a name="information-functions"></a>Fonctions d'information

Appelez les fonctions d’information et d’utilitaire WNet suivantes pour récupérer le fournisseur de réseau et d’autres informations.



| Fonction                                                         | Description                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Retourne le code d’erreur le plus récent défini par une fonction WNet, celui signalé par un fournisseur réseau.  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Retourne des informations étendues sur un fournisseur de réseau spécifique.                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Retourne le nom du fournisseur pour un type spécifique de réseau.                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Retourne le fournisseur réseau qui possède une ressource et obtient des informations sur le type de ressource. |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Retourne le parent d’une ressource réseau.                                                           |



 

## <a name="user-functions"></a>Fonctions utilisateur

Appelez la fonction WNet suivante pour récupérer le nom de l’utilisateur associé à un appareil local.



| Fonction                           | Description                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Retourne le nom d’utilisateur par défaut actuel ou le nom d’utilisateur qui a établi la connexion. |



 

La plupart des fonctions WNET utilisent une structure [**Resource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) pour stocker des informations sur une ressource réseau.

 

 