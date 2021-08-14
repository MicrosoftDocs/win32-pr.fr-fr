---
description: La méthode RenderOutputPins crée la partie aperçu du graphique de filtre.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'IRenderEngine :: RenderOutputPins, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b81ea650d805c8ed2e42797f4dffdd9851eb3f072cff0abb05f54c4581684bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818561"
---
# <a name="irenderenginerenderoutputpins-method"></a>IRenderEngine :: RenderOutputPins, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `RenderOutputPins` méthode crée la partie aperçu du graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                  | Description                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>                                                        |
| <dl> <dt>**VFW \_ S \_ audio \_ non \_ restitué**</dt> </dl>  | Impossible de lire le flux audio.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argument non valide.<br/>                                               |
| <dl> <dt>**le \_ moteur de rendu E \_ \_ est \_ défectueux**</dt> </dl> | L’opération a échoué, car le projet n’a pas été rendu correctement.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>                 | Erreur inattendue.<br/>                                               |



 

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le composant frontal du graphique. Pour effectuer une opération autre que la version préliminaire, n’appelez pas cette méthode. Au lieu de cela, appelez [**IRenderEngine :: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) pour obtenir des pointeurs vers les broches de sortie.

S’il n’y a aucune carte son sur l’ordinateur de l’utilisateur, cette méthode retourne VFW \_ s \_ audio \_ non \_ restitué. Dans ce cas, il n’y aura pas de préversion audio, mais la version préliminaire de la vidéo n’est pas affectée.

Si le code PIN provient d’un groupe vidéo, cette méthode crée une fenêtre vidéo. Le thread appelant doit distribuer les messages (par exemple, pour déplacer la fenêtre ou répondre aux clics de souris dans la zone cliente de la fenêtre).

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




