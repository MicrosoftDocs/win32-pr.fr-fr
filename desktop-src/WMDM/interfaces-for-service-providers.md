---
title: Interfaces pour les fournisseurs de services
description: Interfaces pour les fournisseurs de services
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Gestionnaire de périphériques de support, interfaces du fournisseur de services
- Gestionnaire de périphériques, interfaces du fournisseur de services
- fournisseurs de services, interfaces
- Référence de programmation, interfaces de fournisseur de services
- référence pour les Gestionnaire de périphériques de support Windows, les interfaces de fournisseur de services
- interfaces du fournisseur de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019d31f05674f0d9e492f8a73748500bc1d9d514
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919499"
---
# <a name="interfaces-for-service-providers"></a>Interfaces pour les fournisseurs de services

cette section décrit les interfaces implémentées par les fournisseurs de services Windows Media Gestionnaire de périphériques. les fournisseurs de services effectuent la majeure partie du travail réel de communication avec un appareil, car ils implémentent la plupart des méthodes du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques appelées par l’application.

Les fournisseurs de services n’ont pas besoin d’implémenter toutes les interfaces listées dans cette section. Par exemple, un périphérique multimédia qui n’a pas de stockage intégré n’implémente pas les interfaces utilisées pour contrôler ou exposer du contenu. L’indication d’une méthode ou d’une interface est indiquée sur la page de référence appropriée.



| Interface ou classe                                     | Description                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Classe d’assistance qui permet à un fournisseur de services ou à un fournisseur de contenu sécurisé d’authentifier une application et de créer des signatures MAC pour des paramètres sécurisés.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | fournit au client (généralement Windows Gestionnaire de périphériques de média) un énumérateur d’appareil pour les périphériques que ce fournisseur de services prend en charge.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Étend **IMDServiceProvider** en fournissant une méthode permettant de créer l’appareil à l’aide du chemin d’accès de l’appareil.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Étend **IMDServiceProvider2** en fournissant une méthode pour définir les préférences d’énumération de l’appareil.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Fournit une association basée sur une instance avec un appareil multimédia. À l’aide de cette interface, le client peut énumérer les énumérateurs de supports de stockage pour l’appareil, obtenir des informations sur l’appareil et envoyer des commandes opaques (directes) à l’appareil.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Étend **IMDSPDevice** en fournissant des méthodes pour obtenir des formats vidéo étendus, en obtenant des noms d’appareil plug-and-Play (PNP), en activant l’utilisation de pages de propriétés et en permettant d’obtenir un pointeur vers un support de stockage à partir de son nom. Cette interface est facultative pour le fournisseur de services, mais elle est recommandée. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Étend **IMDSPDevice2** en fournissant la possibilité d’interroger les propriétés et les capacités de l’appareil en ce qui concerne un format d’objet.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Fournit des méthodes pour le contrôle des appareils.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | permet à Windows Gestionnaire de périphériques multimédia de déléguer le transfert de contenu au fournisseur de services. dans ce cas Windows Media Gestionnaire de périphériques n’effectue aucun traitement du contenu avant de l’envoyer au fournisseur de services. Le fournisseur de services obtient le contrôle total de la source.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Énumère les périphériques multimédias pris en charge par ce fournisseur de services.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Énumère les supports de stockage sur un appareil et le contenu sur un support de stockage.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Contient des méthodes pour les opérations de transfert de données sur un objet de stockage.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Étend **IMDSPObject** en fournissant une transmission plus efficace des données compatibles DRM.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Définit ou obtient la longueur de la lecture, la position de lecture, le décalage de lecture ou la longueur totale des objets lisibles sur un support de stockage.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Récupère l’URL à partir de laquelle les composants mis à jour peuvent être téléchargés.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Fournit une association basée sur des instances avec un support de stockage sur un appareil. Cette interface crée des objets de stockage, récupère des informations les concernant et donne accès à l’interface **IMDSPEnumStorage** pour énumérer les sous-dossiers imbriqués dans le stockage actuel.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Étend les **IMDSPStorage** en obtenant et en définissant des attributs étendus et en permettant d’obtenir un pointeur vers le stockage à partir de son nom.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Étend **IMDSPStorage2** en prenant en charge les métadonnées.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Étend **IMDSPStorage3** en prenant en charge les objets playlist.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Récupère des informations globales sur un support de stockage, telles que la quantité d’espace libre et le nombre total de fichiers.                                                                                                                                                                                              |



 

Le diagramme suivant montre comment obtenir les différentes interfaces implémentées par un fournisseur de services. Dans ce diagramme, les interfaces dérivées sont affichées dans la même balise pour la compacité. par conséquent, IMDServiceProvider/2/3 représente trois interfaces : **IMDServiceProvider**, **IMDServiceProvider2** et **IMDServiceProvider3**. Les méthodes indiquées sont étendues par une seule de ces interfaces. Les interfaces dérivées sont obtenues en appelant **QueryInterface** sur l’interface de base de l’objet créé.

![Diagramme montrant comment le gestionnaire de périphériques Windows Media s’attend à obtenir des interfaces à partir d’un fournisseur de services.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> <dt>

[**Windows Interfaces de DRM-Implemented de média**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




