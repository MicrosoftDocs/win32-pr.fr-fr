---
description: La méthode BufferCB est une méthode de rappel qui reçoit un pointeur vers l’exemple de mémoire tampon.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'ISampleGrabberCB :: BufferCB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224361"
---
# <a name="isamplegrabbercbbuffercb-method"></a>ISampleGrabberCB :: BufferCB, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La méthode **BufferCB** est une méthode de rappel qui reçoit un pointeur vers l’exemple de mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SampleTime* 
</dt> <dd>

Heure de début de l’échantillon, en secondes.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient les exemples de données. Le format des données dépend du type de support de la broche d’entrée de l’exemple de la accroche. Pour accéder au type de média, appelez [**ISampleGrabber :: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*BufferLen* 
</dt> <dd>

Longueur de la mémoire tampon vers laquelle pointe *pbuffer*, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite, ou un code d’erreur **HRESULT** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode de rappel reçoit un pointeur vers les données dans l’exemple de média le plus récent.

> [!Note]  
> Cette méthode reçoit un pointeur vers les données d’exemple d’origine, pas une copie. La documentation d’origine a indiqué de manière incorrecte que *pbuffer* contient une copie des données.

 

Pour configurer le rappel, appelez [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md).

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




