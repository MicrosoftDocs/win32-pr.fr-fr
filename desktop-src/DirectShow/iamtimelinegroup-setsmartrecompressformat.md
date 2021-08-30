---
description: La méthode SetSmartRecompressFormat spécifie un format de compression vidéo à utiliser pour la recompression intelligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'IAMTimelineGroup :: SetSmartRecompressFormat, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8bf19ee67c08fc674681ade174966fe415a950103099011f52102e8c6edede7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083879"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>IAMTimelineGroup :: SetSmartRecompressFormat, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetSmartRecompressFormat` méthode spécifie un format de compression vidéo à utiliser pour la recompression intelligente.

La recompression intelligente n’est pas prise en charge pour les groupes audio.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFormat* 
</dt> <dd>

Pointeur vers une structure décrivant le format de compression. Actuellement, seule la structure [**SCompFmt0**](scompfmt0.md) est valide. Vous devez effectuer un cast de ce paramètre en un pointeur de type **long**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, appelez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) sur le même groupe pour spécifier un format non compressé.

Si la `SetSmartRecompressFormat` méthode est réussie, vous pouvez utiliser le moteur de rendu intelligent pour générer un flux vidéo compressé. La vidéo compressée aura la largeur, la hauteur et la fréquence d’images spécifiées dans le paramètre *pFormat* . Ces valeurs remplaceront celles données pour le format non compressé dans la méthode **SetMediaType** . Toutefois, pour bénéficier des avantages de la recompression intelligente, les deux formats doivent correspondre. En d’autres termes, les formats compressés et non compressés doivent avoir la même hauteur, largeur et fréquence d’images.

Si le moteur de rendu intelligent ne peut pas produire le format compressé, il génère un flux vidéo non compressé à la place. Si cela se produit, le moteur de rendu intelligent signale une \_ erreur de rendu de compresseur de l’ID DEX \_ \_ introuvable \_ pendant la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) . L’application peut intercepter cette erreur par le biais de la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) . (Pour plus d’informations, consultez [journalisation des erreurs](logging-errors.md) et des [Erreurs de rendu](rendering-errors.md).)

Le format de recompression intelligente n’est pas persistant. Si une application utilise la recompression intelligente, elle doit définir le format de recompression chaque fois qu’elle charge un fichier projet.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[Moteur de rendu intelligent](smart-render-engine.md)
</dt> <dt>

[écriture d’un Project dans un fichier](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




