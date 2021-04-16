---
title: Obtention de la bibliothèque DRM requise
description: Obtention de la bibliothèque DRM requise
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- Windows Media Format SDK, obtention des bibliothèques DRM requises
- ASF (Advanced Systems Format), obtention des bibliothèques DRM requises
- ASF (Advanced Systems Format), obtention des bibliothèques DRM requises
- gestion des droits numériques (DRM), obtention des bibliothèques requises
- DRM (Digital Rights Management), obtention des bibliothèques requises
- gestion des droits numériques (DRM), informations de build
- DRM (gestion des droits numériques), informations de build
- gestion des droits numériques (DRM), informations de débogage
- DRM (gestion des droits numériques), informations de débogage
- débogage DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383131"
---
# <a name="obtaining-the-required-drm-library"></a>Obtention de la bibliothèque DRM requise

Pour créer ou lire des fichiers multimédias numériques protégés par DRM, votre application doit être liée à une bibliothèque statique qui est fournie sous forme binaire par Microsoft. Cette bibliothèque est parfois appelée bibliothèque stub ou « stublib » et identifie de manière unique votre application.

Dans cette documentation, la bibliothèque DRM est appelée « WMStubDRM. lib ». Le nom de la bibliothèque que vous recevez comportera un numéro d’identification. Pour obtenir cette bibliothèque, vous devez signer un contrat de licence auprès de Microsoft. Les termes du contrat peuvent varier selon que vous demandez une licence d’évaluation ou une licence de production. Pour plus d’informations sur le processus de gestion de licences DRM, consultez le formulaire Windows Media Licensing sur le [site Web de Microsoft](https://www.microsoft.com/licensing/default).

La bibliothèque que vous recevez a un niveau de sécurité DRM qui dépend du type de contrat de licence que vous entrez. Une licence DRM peut restreindre l’accès au contenu des fichiers aux applications avec des composants DRM situés sous un niveau de sécurité spécifié. Ce niveau de sécurité n’est pas le même que le niveau de individualisation DRM, et n’est pas lié aux valeurs numériques des niveaux de protection de sortie (OPLs). Le tableau suivant présente des exemples de niveaux de sécurité DRM pour différents lecteurs et périphériques portables.



| Niveau de sécurité | Lecteurs et appareils mobiles                                                                                                                                                                                                                                                                                                   | Exemple                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | Appareils qui ne prennent pas en charge Windows Media DRM. La protection DRM est supprimée lorsque le contenu est transféré vers un tel appareil.                                                                                                                                                                                                         | Appareils qui prennent en charge le contenu Windows Media mais pas le contenu protégé                                                                                                                       |
| 1 000          | Applications de lecteur basées sur le kit de développement logiciel (SDK) Windows Media Format 9,5 ou version antérieure qui ne répondent pas à des exigences supplémentaires pour le niveau 2000. appareils basés sur le périphérique portable Windows Media DRM v1.<br/> Appareils basés sur Windows CE 4,2 et versions ultérieures.<br/>                                                                       | Lecteur Windows Media 6,4, lecteur Windows Media 7Portable les appareils multimédias qui prennent en charge Windows Media Mobile Device DRM v1.<br/>                                                             |
| 2 000          | Applications de lecteur basées sur le kit de développement logiciel (SDK) Windows Media Format 9 Series ou version ultérieure, et qui suivent un ensemble plus strict d’instructions de protection du contenu que les applications au niveau 1 000. appareils basés sur Windows Media DRM 10 pour appareils mobiles.<br/> Appareils basés sur Windows Media DRM 10 pour les périphériques réseau.<br/> | Appareils Windows Media Player 9 Series et laterPortable Media qui prennent en charge Windows Media DRM 10 pour les appareils mobiles<br/> Appareils Media Center portables basés sur Windows Mobile<br/> |



 

## <a name="build-and-debugging-information"></a>Informations de génération et de débogage

Lorsque vous effectuez un lien vers WMStubDRM. lib, ne liez pas à wmvcore. lib. Le composant DRM ne fonctionnera pas correctement si l’application est liée aux deux bibliothèques.

Un point d’arrêt de l’utilisateur dans le composant DRM empêche à la fois les versions Debug et Release des applications d’accéder au contenu protégé lors de l’exécution à l’intérieur du débogueur. Pour résoudre les problèmes liés aux fonctions DRM dans votre application, vous devez écrire vos propres routines de suivi qui enregistrent des informations telles que des valeurs **HRESULT** à un emplacement tel qu’un fichier journal.

Si vous tentez d’exécuter une version Release d’une application sur un système avec une version de débogage du kit de développement logiciel (SDK) installé (ou l’inverse), vous rencontrerez des erreurs de segment de mémoire lors de la lecture du contenu DRM version 7. Veillez à exécuter des applications de débogage sur les bits du SDK de débogage et à publier des applications sur les bits de version. Le même problème se produit si vous exécutez une version de débogage du kit de développement logiciel (SDK) avec un composant DRM individualisé (qui est toujours une version Release).

**Notes** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

Les fichiers WMStubDRM. lib associés au kit de développement logiciel (SDK) Windows Media Format 9,5 peuvent être utilisés uniquement avec les composants de Microsoft Visual Studio .NET 2003. Si vous utilisez une version antérieure de la bibliothèque stub, il n’existe aucune nouvelle restriction pour son utilisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 





