---
title: Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques 11
description: Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Gestionnaire de périphériques Windows Media, à propos de
- Gestionnaire de périphériques, à propos de
- Protocole MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- Classe de stockage de masse (MSC)
- MSC (classe de stockage de masse)
- Windows Media Gestionnaire de périphériques, applications de bureau
- Gestionnaire de périphériques, applications de bureau
- applications de bureau, à propos de
- Gestionnaire de périphériques Windows Media, fournisseurs de services
- Gestionnaire de périphériques, fournisseurs de services
- fournisseurs de services, à propos de
- Gestionnaire de périphériques Windows Media, plug-ins
- Gestionnaire de périphériques, plug-INSP
- plug-ins, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383124"
---
# <a name="windows-media-device-manager-11-sdk"></a>Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques 11

> [!IMPORTANT]
> Les API Windows Media Gestionnaire de périphériques sont désormais incluses dans le SDK Windows. Aucun téléchargement supplémentaire du SDK n’est nécessaire.

 

Le kit de développement logiciel (SDK) Microsoft Windows Media Gestionnaire de périphériques vous permet de créer des applications de bureau et des composants qui peuvent communiquer avec des appareils mobiles connectés. Windows Media Gestionnaire de périphériques permet à votre application ou composant d’énumérer, d’explorer et d’échanger des fichiers avec un appareil, de rechercher des métadonnées et de demander des informations sur le nombre de jeux. Les applications ou composants basés sur Windows Media Gestionnaire de périphériques ont une API cohérente pour communiquer avec un large éventail d’appareils, notamment le protocole MTP (Media Transfer Protocol), la classe de stockage de masse (MSC), l’RAPI et d’autres périphériques basés sur les versions les plus récentes et les plus anciennes de la technologie Windows Media.

Vous pouvez créer les éléments suivants à l’aide du kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media :

-   Applications de bureau, telles que des lecteurs multimédias personnalisés. Toutes les communications entre une application et un appareil mobile doivent traverser Windows Media Gestionnaire de périphériques, qui agit en tant que service Broker entre l’application, le système de gestion des droits numériques Microsoft et le fournisseur de services.
-   Fournisseurs de services, qui jouent le rôle de lien de communication entre un appareil personnalisé et une application de bureau. Bien que Microsoft fournisse un certain nombre de fournisseurs de services qui peuvent communiquer avec la plupart des appareils prêts à l’emploi, vous pouvez créer un fournisseur de services personnalisé pour personnaliser la communication entre un appareil et une application de bureau.
-   Des plug-ins, qui peuvent effectuer des tâches telles que la demande et la journalisation des nombres de lecture sur les appareils. Ces plug-ins peuvent être joints à d’autres applications de bureau, telles que le lecteur Windows Media, pour envoyer des informations aux fournisseurs de contenu afin de gérer les paiements de droits d’auteur.

Pour télécharger le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques, consultez [la page de téléchargement Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) sur le site Web MSDN.

Ce kit de développement logiciel (SDK) est un composant du kit de développement logiciel (SDK) Microsoft Windows Media. Les autres composants incluent le SDK Windows Media format, le kit de développement logiciel (SDK) Windows Media Services, le SDK Windows Media Encoder, le kit de développement logiciel (SDK) Windows Media Rights Manager et le kit de développement logiciel (SDK) Windows Media Player

Cette documentation contient les sections suivantes.



| Section                                            | Description                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prise en main](getting-started.md)             | Décrit les nouveautés de cette version de Windows Media Gestionnaire de périphériques, offre une vue d’ensemble du fonctionnement de Windows Media Gestionnaire de périphériques, décrit les éléments nécessaires au développement d’une application ou d’un fournisseur de services, et décrit les exemples fournis avec le kit de développement logiciel (SDK). |
| [Guide de programmation](programming-guide.md)         | Explique comment créer des applications et des fournisseurs de services.                                                                                                                                                                                                      |
| [Guide de référence de programmation](programming-reference.md) | Fournit des informations de référence sur C++ pour les interfaces, les méthodes, les classes et les structures prises en charge par le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media.                                                                                                                      |
| [*Glossaire*](wmdm-glossary.md)                    | Définit les termes utilisés dans cette documentation.                                                                                                                                                                                                                       |



 

 

 




