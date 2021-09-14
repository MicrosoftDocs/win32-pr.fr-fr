---
title: Windows Kit de développement logiciel (SDK) Media Gestionnaire de périphériques 11
description: Windows Kit de développement logiciel (SDK) Media Gestionnaire de périphériques 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Gestionnaire de périphériques de média, à propos de
- Gestionnaire de périphériques, à propos de
- Protocole MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- classe de Stockage de masse (MSC)
- MSC (classe Stockage de masse)
- Windows Gestionnaire de périphériques de média, applications de bureau
- Gestionnaire de périphériques, applications de bureau
- applications de bureau, à propos de
- Windows Gestionnaire de périphériques de support, fournisseurs de services
- Gestionnaire de périphériques, fournisseurs de services
- fournisseurs de services, à propos de
- Windows Gestionnaire de périphériques de média, plug-ins
- Gestionnaire de périphériques, plug-INSP
- plug-ins, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217156"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows Kit de développement logiciel (SDK) Media Gestionnaire de périphériques 11

> [!IMPORTANT]
> les api Windows Media Gestionnaire de périphériques sont désormais incluses dans le SDK Windows. Aucun téléchargement supplémentaire du SDK n’est nécessaire.

 

le kit de développement logiciel (SDK) de Microsoft Windows Media Gestionnaire de périphériques vous permet de créer des applications de bureau et des composants qui peuvent communiquer avec des appareils mobiles connectés. Windows Media Gestionnaire de périphériques permet à votre application ou composant d’énumérer, d’explorer et d’échanger des fichiers avec un appareil, de rechercher des métadonnées et de demander des informations sur le nombre de jeux. les Applications ou composants basés sur Windows Media Gestionnaire de périphériques disposent d’une API cohérente pour communiquer avec un large éventail d’appareils, notamment MTP (Media Transfer Protocol), MSC (Mass Stockage Class), RAPI et d’autres appareils basés sur les versions les plus récentes de Windows Media technology.

vous pouvez créer les éléments suivants à l’aide du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques :

-   Applications de bureau, telles que des lecteurs multimédias personnalisés. toutes les communications entre une application et un appareil mobile doivent traverser Windows Media Gestionnaire de périphériques, qui agit en tant que service broker entre l’application, le système de gestion des droits numériques Microsoft et le fournisseur de services.
-   Fournisseurs de services, qui jouent le rôle de lien de communication entre un appareil personnalisé et une application de bureau. Bien que Microsoft fournisse un certain nombre de fournisseurs de services qui peuvent communiquer avec la plupart des appareils prêts à l’emploi, vous pouvez créer un fournisseur de services personnalisé pour personnaliser la communication entre un appareil et une application de bureau.
-   Des plug-ins, qui peuvent effectuer des tâches telles que la demande et la journalisation des nombres de lecture sur les appareils. ces plug-ins peuvent être joints à d’autres applications de bureau, telles que le Lecteur Windows Media pour envoyer des informations aux fournisseurs de contenu afin de gérer les paiements de droits d’auteur.

pour télécharger le kit de développement logiciel (SDK) Windows media Gestionnaire de périphériques, consultez [la page de téléchargement Windows media](https://msdn.microsoft.com/windows/desktop/aa904949) sur le site Web MSDN.

ce kit de développement logiciel (SDK) est un composant du kit de développement logiciel Microsoft Windows Media. les autres composants incluent le kit de développement logiciel (sdk) Windows media Format, le Services Windows Media sdk, Windows le kit de développement logiciel (sdk) media encoder, Windows le kit de développement logiciel (sdk) media Rights Manager et Lecteur Windows Media le kit de développement logiciel

Cette documentation contient les sections suivantes.



| Section                                            | Description                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prise en main](getting-started.md)             | décrit les nouveautés de cette version de Windows media Gestionnaire de périphériques, donne une vue d’ensemble de la façon dont Windows media Gestionnaire de périphériques fonctionne, décrit ce qui est nécessaire pour développer un fournisseur d’applications ou de services, et décrit les exemples fournis avec le kit de développement logiciel (SDK). |
| [Guide de programmation](programming-guide.md)         | Explique comment créer des applications et des fournisseurs de services.                                                                                                                                                                                                      |
| [Guide de référence de programmation](programming-reference.md) | fournit des informations de référence C++ pour les interfaces, les méthodes, les classes et les structures prises en charge par le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media.                                                                                                                      |
| [*Glossaire*](wmdm-glossary.md)                    | Définit les termes utilisés dans cette documentation.                                                                                                                                                                                                                       |



 

 

 




