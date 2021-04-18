---
description: L’interface IAMTimeline fournit des méthodes pour manipuler la chronologie, l’objet central dans les services d’édition Microsoft DirectShow (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interface IAMTimeline (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540648"
---
# <a name="iamtimeline-interface"></a>Interface IAMTimeline

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimeline` interface fournit des méthodes pour manipuler la chronologie, l’objet central dans les [services d’édition Microsoft DirectShow](directshow-editing-services.md) (des). Une chronologie est une collection d’éléments chronologiques, tels que des clips vidéo, des clips audio, des effets et des transitions entre des éléments. Le moteur de rendu utilise la chronologie pour créer un graphique de filtre, à partir duquel l’application peut générer la sortie rendue.

`IAMTimeline` effectue trois services de base. Informatique

-   Crée les objets dans la chronologie.
-   Agit comme un conteneur pour ces objets.
-   Définit et récupère les paramètres généraux de la chronologie.

Pour créer l’objet Timeline, appelez **CoCreateInstance** avec l’identificateur de classe CLSID \_ AMTimeline.

## <a name="members"></a>Membres

L’interface **IAMTimeline** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimeline** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimeline** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**AddGroup**](iamtimeline-addgroup.md)                           | Ajoute un groupe à la chronologie.<br/>                                                                                          |
| [**ClearAllGroups**](iamtimeline-clearallgroups.md)               | Supprime tous les groupes de la chronologie, ainsi que tous les objets contenus dans ces groupes.<br/>                                |
| [**CreateEmptyNode**](iamtimeline-createemptynode.md)             | Crée un nouvel objet Timeline.<br/>                                                                                         |
| [**EffectsEnabled**](iamtimeline-effectsenabled.md)               | Détermine si les effets sont activés.<br/>                                                                                |
| [**EnableEffects**](iamtimeline-enableeffects.md)                 | Active ou désactive tous les effets de la chronologie.<br/>                                                                       |
| [**EnableTransitions**](iamtimeline-enabletransitions.md)         | Active ou désactive toutes les transitions dans la chronologie.<br/>                                                                   |
| [**GetCountOfType**](iamtimeline-getcountoftype.md)               | Récupère le nombre d’objets du type spécifié qui sont contenus dans un groupe spécifié et tous ses enfants.<br/> |
| [**GetDefaultEffect**](iamtimeline-getdefaulteffect.md)           | Récupère l’effet par défaut.<br/>                                                                                          |
| [**GetDefaultEffectB**](iamtimeline-getdefaulteffectb.md)         | Récupère l’effet par défaut sous la forme d’une valeur **BSTR** .<br/>                                                                      |
| [**GetDefaultFPS**](iamtimeline-getdefaultfps.md)                 | Récupère la fréquence d’images de sortie par défaut, en images par seconde.<br/>                                                         |
| [**GetDefaultTransition**](iamtimeline-getdefaulttransition.md)   | Récupère la transition par défaut.<br/>                                                                                      |
| [**GetDefaultTransitionB**](iamtimeline-getdefaulttransitionb.md) | Récupère la transition par défaut sous la forme d’une valeur **BSTR** .<br/>                                                                  |
| [**GetDirtyRange**](iamtimeline-getdirtyrange.md)                 | Non pris en charge.<br/>                                                                                                         |
| [**GetDuration**](iamtimeline-getduration.md)                     | Récupère la durée de la chronologie.<br/>                                                                                       |
| [**GetDuration2**](iamtimeline-getduration2.md)                   | Récupère la durée de la chronologie sous la forme d’un **double**.<br/>                                                                       |
| [**GetGroup**](iamtimeline-getgroup.md)                           | Récupère un groupe spécifié.<br/>                                                                                           |
| [**GetGroupCount**](iamtimeline-getgroupcount.md)                 | Récupère le nombre de groupes contenus dans la chronologie.<br/>                                                     |
| [**GetInsertMode**](iamtimeline-getinsertmode.md)                 | Non pris en charge.<br/>                                                                                                         |
| [**IsDirty**](iamtimeline-isdirty.md)                             | Non pris en charge.<br/>                                                                                                         |
| [**RemGroupFromList**](iamtimeline-remgroupfromlist.md)           | Non pris en charge.<br/>                                                                                                         |
| [**SetDefaultEffect**](iamtimeline-setdefaulteffect.md)           | Définit l’effet par défaut.<br/>                                                                                               |
| [**SetDefaultEffectB**](iamtimeline-setdefaulteffectb.md)         | Définit l’effet par défaut en tant que valeur **BSTR** .<br/>                                                                           |
| [**SetDefaultFPS**](iamtimeline-setdefaultfps.md)                 | Définit la fréquence d’images de sortie par défaut, en images par seconde.<br/>                                                              |
| [**SetDefaultTransition**](iamtimeline-setdefaulttransition.md)   | Définit la transition par défaut.<br/>                                                                                           |
| [**SetDefaultTransitionB**](iamtimeline-setdefaulttransitionb.md) | Définit la transition par défaut en tant que valeur BSTR.<br/>                                                                           |
| [**SetInsertMode**](iamtimeline-setinsertmode.md)                 | Non implémenté.<br/>                                                                                                       |
| [**SetInterestRange**](iamtimeline-setinterestrange.md)           | Non implémenté.<br/>                                                                                                       |
| [**TransitionsEnabled**](iamtimeline-transitionsenabled.md)       | Détermine si les transitions sont activées.<br/>                                                                            |
| [**ValidateSourceNames**](iamtimeline-validatesourcenames.md)     | Valide les noms de sources dans la chronologie.<br/>                                                                                |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
