---
description: La méthode SetMediaTimes définit les heures de démarrage et d’arrêt du support.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'IAMTimelineSrc :: SetMediaTimes, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539958"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>IAMTimelineSrc :: SetMediaTimes, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetMediaTimes` méthode définit les heures de démarrage et d’arrêt du support.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Start* 
</dt> <dd>

Heure de début du média, en unités de 100 nanosecondes.

</dd> <dt>

*Stop* 
</dt> <dd>

Heure d’arrêt du support, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les heures de support sont les heures d’arrêt et de démarrage relatives au fichier multimédia d’origine. Définissez toujours les temps de support lorsque vous ajoutez une source vidéo ou audio à la chronologie. Dans le cas contraire, des problèmes de rendu peuvent se produire. L’heure d’arrêt doit être postérieure à l’heure de début.

Pour utiliser une image continue d’une source vidéo, définissez l’heure d’arrêt sur une valeur fractionnaire supérieure à l’heure de début, par exemple 100 nanosecondes. La définition de la même valeur provoque une erreur de rendu.

Si la durée de la chronologie ne correspond pas à la durée du support, la source est étirée ou réduite en conséquence. Cela provoque une lecture plus lente ou plus rapide du clip que la vitesse de création. (Le décalage de la hauteur se produit dans une source audio.) Pour plus d’informations, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).

Vous pouvez spécifier la durée du fichier source en appelant la méthode [**SetMediaLength**](iamtimelinesrc-setmedialength.md) . Si vous définissez une heure d’arrêt de support qui dépasse la durée, est tronque l’heure d’arrêt.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




