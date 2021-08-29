---
description: Une erreur récupérable s’est produite lors de la diffusion en continu.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Événement MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce62dd48ad9e8fdcbfbbce4b5eb1d29af780508cdf66ac857d05237f1294a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061884"
---
# <a name="menonfatalerror-event"></a>Événement MENonFatalError

Une erreur récupérable s’est produite lors de la diffusion en continu. Tout composant Media Foundation peut envoyer cet événement à tout moment.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE            | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| VT \_ UI4<br/> | Valeur **HRESULT** qui décrit l’erreur.<br/> <br/> |



## <a name="attributes"></a>Attributs

Aucun attribut n’est défini pour cet événement.

## <a name="remarks"></a>Remarques

Cet événement signale une erreur inattendue mais récupérable pendant la diffusion en continu. Par exemple, une source de média peut envoyer cet événement si elle supprime un paquet.

N’envoyez pas cet événement pour signaler qu’une méthode asynchrone a échoué. Si une méthode asynchrone échoue, le code d’erreur est retourné dans l’événement normal pour cette méthode.

Si une erreur de diffusion en continu non récupérable se produit, envoyez l’événement [MEError](meerror.md) .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




