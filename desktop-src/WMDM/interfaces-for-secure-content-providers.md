---
title: Interfaces pour les fournisseurs de contenu sécurisés
description: Interfaces pour les fournisseurs de contenu sécurisés
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Gestionnaire de périphériques de média, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Référence de programmation, contenu protégé par DRM
- référence pour Windows Gestionnaire de périphériques de média, contenu protégé par DRM
- Contenu protégé par DRM
- Windows Gestionnaire de périphériques de média, fournisseur de contenu sécurisé (SCP)
- Gestionnaire de périphériques, fournisseur de contenu sécurisé (SCP)
- Référence de programmation, fournisseur de contenu sécurisé (SCP)
- référence pour Windows Media Gestionnaire de périphériques, secure content provider (SCP)
- fournisseur de contenu sécurisé (SCP)
- SCP (Secure Content Provider)
- Windows Gestionnaire de périphériques de média, interfaces SCP
- Gestionnaire de périphériques, interfaces SCP
- Référence de programmation, interfaces SCP
- référence pour Windows Gestionnaire de périphériques de média, interfaces SCP
- Interfaces SCP, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919500"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfaces pour les fournisseurs de contenu sécurisés

un fournisseur de contenu sécurisé (SCP) est un composant de plug-in qui permet à Windows Media Gestionnaire de périphériques de transférer et de demander des informations de droits à un contenu protégé par DRM. Microsoft fournit un composant SCP qui peut gérer des fichiers WMA et WMV protégés par DRM. Si votre appareil ou votre application utilise le contenu protégé par DRM d’autres formats, il doit créer un composant SCP en implémentant toutes ces interfaces. Dans le cas contraire, vous n’aurez pas besoin d’utiliser ces interfaces.



| Interface                                                  | Description                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | Interface principale du fournisseur de contenu sécurisé.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Étend **ISCPSecureAuthenticate** en fournissant un moyen d’obtenir un objet de session.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Utilisé pour échanger du contenu sécurisé et des droits associés au contenu.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Étend **ISCPSecureExchange** en fournissant une nouvelle version de la méthode **TransferContainerData** .                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Étend **ISCPSecureExchange2** en fournissant des performances d’échange de données améliorées et une méthode de rappel de transfert complet.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | interrogé par Windows Gestionnaire de périphériques multimédia pour déterminer la propriété du contenu sécurisé.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Étend **ISCPSecureQuery** via une fonctionnalité qui détermine si le fournisseur de contenu sécurisé est responsable du contenu et, le cas échéant, fournit une URL pour mettre à jour les composants révoqués et déterminer les composants qui ont été révoqués. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Étend **ISCPSecureQuery2** en fournissant un ensemble de nouvelles méthodes pour récupérer les droits et prendre une décision sur un canal clair.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Fournit une gestion efficace de l’État commun pour plusieurs opérations.                                                                                                                                                                                  |



 

 

 




