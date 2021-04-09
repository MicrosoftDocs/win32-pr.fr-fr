---
title: Individualiser des applications DRM
description: Individualiser des applications DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media Format SDK, individualisation des applications DRM
- Windows Media Format SDK, application individualisation
- ASF (Advanced Systems Format), individualisation des applications DRM
- ASF (format des systèmes avancés), individualisation des applications DRM
- ASF (Advanced Systems Format), application d’individualisation
- ASF (format des systèmes avancés), individualisation des applications
- gestion des droits numériques (DRM), individualisation des applications
- DRM (gestion des droits numériques), individualisation des applications
- gestion des droits numériques (DRM), individualisation des applications
- DRM (gestion des droits numériques), individualisation des applications
- individualisation de l’application
- individualiser des applications DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103940752"
---
# <a name="individualizing-drm-applications"></a>Individualiser des applications DRM

Pour accroître la sécurité, le composant DRM des applications peut être *individualisé*. Une application individualisée est une application qui a reçu une mise à niveau vers ses composants DRM qui la différencie de toutes les autres copies de la même application. Les propriétaires de contenu peuvent exiger que leurs fichiers protégés soient lus uniquement sur une application qui a été individualisée.

Le processus d’individualisation démarre lorsque l’application contacte le service d’individualisation Microsoft, qui installe ensuite une mise à niveau de sécurité sur l’ordinateur de l’utilisateur. Étant donné que le service d’individualisation gère les informations de l’utilisateur, vous devez afficher la politique de confidentialité de Microsoft ou fournir un lien vers cette page sur le site Web de Microsoft : <https://privacy.microsoft.com/privacystatement> .

L’individualisation peut être effectuée de différentes façons. Par exemple, une individualisation peut avoir lieu lorsqu’un utilisateur lit un fichier protégé. La demande de licence est envoyée au [*service de licence Windows Media*](wmformat-glossary.md), qui inspecte le certificat de l’application demandant la [*licence*](wmformat-glossary.md). Si le composant DRM de l’application n’a pas été individualisé, le service de licence Windows Media refuse d’émettre la licence, car il s’agit de la stratégie du service de licence Windows Media pour émettre des licences uniquement pour des joueurs individuels. L’application peut ensuite informer l’utilisateur que l’application doit être mise à niveau. Si l’utilisateur accepte, une mise à niveau de sécurité est fournie pour individualiser le composant DRM de l’application.

Pour une meilleure expérience utilisateur, vous pouvez lancer le processus d’individualisation comme étape de mise à niveau de la sécurité lors de l’installation. l’utilisateur n’est alors pas interrompu pour obtenir une mise à niveau de sécurité lors de la tentative de lecture d’un fichier protégé. Vous pouvez également encourager activement l’individualisation en ajoutant une commande de menu ou un bouton de **mise à niveau de sécurité** à l’application.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




