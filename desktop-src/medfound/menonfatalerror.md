---
description: Une erreur récupérable s’est produite lors de la diffusion en continu.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Événement MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318825"
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

## <a name="remarks"></a>Notes

Cet événement signale une erreur inattendue mais récupérable pendant la diffusion en continu. Par exemple, une source de média peut envoyer cet événement si elle supprime un paquet.

N’envoyez pas cet événement pour signaler qu’une méthode asynchrone a échoué. Si une méthode asynchrone échoue, le code d’erreur est retourné dans l’événement normal pour cette méthode.

Si une erreur de diffusion en continu non récupérable se produit, envoyez l’événement [MEError](meerror.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




