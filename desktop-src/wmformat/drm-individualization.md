---
title: Individualisation DRM
description: Individualisation DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK, individualisation DRM
- gestion des droits numériques (DRM), individualisation
- DRM (gestion des droits numériques), individualisation
- individualisation de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196015"
---
# <a name="drm-individualization"></a>Individualisation DRM

les propriétaires de contenu protégé peuvent obliger les utilisateurs à mettre à niveau certains des composants de gestion des droits numériques (DRM) inclus dans le kit de développement logiciel (SDK) Windows Media Format avant d’accéder à leur contenu. Si un utilisateur accepte la mise à niveau, une version individualisée d’un fichier de sécurité (une unique sur son ordinateur) est téléchargée à partir d’un site Web Microsoft. Si l’utilisateur refuse la mise à niveau, il ne pourra pas accéder au contenu. Toutefois, ils pourront toujours accéder au contenu non protégé et au contenu protégé qui ne nécessite pas la mise à niveau. L’exécution d’une mise à niveau de sécurité permet d’augmenter le niveau de protection offert par DRM.

L’individualisation peut être effectuée au moment de l’installation ou lorsqu’une application rencontre pour la première fois un fichier ASF protégé qui l’exige. Étant donné que ce processus modifie les composants système d’un utilisateur, l’application doit avertir l’utilisateur et obtenir son consentement avant d’effectuer la mise à niveau. par exemple, Microsoft Lecteur Windows Media affiche une boîte de dialogue avec le texte suivant :

**Mise à niveau de sécurité requise**

**Le propriétaire du contenu protégé auquel vous essayez d’accéder nécessite d’abord la mise à niveau de certains composants de gestion des droits numériques (DRM) Microsoft sur votre ordinateur.**

**Cliquez sur OK pour mettre à niveau vos composants DRM.**

**Plus**

**Lorsque vous cliquez sur OK, un identificateur unique et un fichier de sécurité DRM sont envoyés à un service Microsoft sur Internet. Le fichier est remplacé par une version personnalisée qui contient votre identificateur unique. Cela augmente le niveau de protection fourni par DRM.**

Toute application prenant en charge l’individualisation doit utiliser la même formulation ou une autre formulation similaire. Pour plus d’informations sur la politique de confidentialité de Microsoft, consultez la section [déclaration de confidentialité](privacy-statement.md) de cette documentation.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Individualiser des applications DRM**](individualizing-drm-applications.md)
</dt> </dl>

 

 




