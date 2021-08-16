---
title: Composant de noyau DRM (déconseillé)
description: Composant de noyau DRM (déconseillé)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Windows Media Format SDK, composant de noyau DRM
- gestion des droits numériques (DRM), composant de noyau
- DRM (gestion des droits numériques), composant de noyau
- Microsoft Secure audio Path (SAP), composant noyau DRM
- Chemin audio sécurisé (SAP), composant de noyau DRM
- SAP (chemin d’accès audio sécurisé), composant de noyau DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8db4389d9156ef13d9e87983a4ae433e6028805268f3cbd55690d4d0d8144b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845756"
---
# <a name="the-drm-kernel-component-deprecated"></a>Composant de noyau DRM (déconseillé)

Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.

Dans le modèle Microsoft Secure audio Path (SAP), le composant de noyau DRM fournit deux fonctionnalités de base qui protègent l’intégrité de la musique chiffrée.

Tout d’abord, le composant client DRM et le composant de noyau DRM sont en communication lorsqu’un fichier musical est lu. Cette communication entre les composants empêche quiconque de falsifier le signal chiffré ou d’insérer des informations erronées.

Deuxièmement, le composant de noyau DRM ne déchiffre pas le signal musical tant que tous les composants restants n’ont pas été authentifiés. Autrement dit, avant de déchiffrer le contenu et de le passer au composant système suivant, le composant de noyau DRM vérifie chaque composant qui reste dans le chemin d’accès à la carte son (chaque composant pouvant accéder au contenu) et vérifie que ces composants sont signés avec un certificat de Microsoft. Un composant non signé peut indiquer un composant suspect ou un pilote malveillant. Ainsi, lorsque le composant de noyau DRM valide les composants restants, si un composant échoue à ce test, le signal s’arrête et ne peut pas être lu. Dans le cas contraire, si tous les composants sont validés, le composant de noyau DRM déchiffre la musique et le transmet au composant suivant.

Microsoft signe numériquement les pilotes qui passent le Windows® tests WHQL (Hardware quality Lab) pour assurer aux utilisateurs qu’ils utilisent les pilotes de qualité supérieure. Cette pratique est standard et garantit l’authenticité des composants, car la signature ne peut pas être falsifiée et le code ne peut pas être modifié sans détruire la signature. Les pilotes certifiés pour le chemin d’accès audio sécurisé doivent protéger les données audio qu’ils traitent de l’accès par des composants non fiables. 

les pilotes inclus dans Windows Millennium Edition et Windows XP sont mis à jour pour le chemin Audio sécurisé et signé. les pilotes qui ne sont pas signés pour une utilisation avec Windows Me ou Windows XP ne peuvent pas lire de musique protégée. Les fabricants de pilotes peuvent réémettre des versions mises à jour de leurs pilotes qui sont signés par WHQL et les publier sur Internet pour que les clients puissent les télécharger.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Chemin d’accès audio sécurisé Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




