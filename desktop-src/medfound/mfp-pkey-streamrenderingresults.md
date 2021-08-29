---
description: Spécifie les flux qui ont été connectés correctement à un récepteur multimédia.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: MFP_PKEY_StreamRenderingResults, propriété (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d63272662d71e261374f51c0463c0bbbb6d515dfeea8dd1ec5ab424609c386d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954709"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>\_Propriété StreamRenderingResults de la propriété HYPERmfp \_

> [!IMPORTANT]
> Action déconseillée. Cette API peut être supprimée des futures versions de Windows. Les applications doivent utiliser la [session multimédia](media-session.md) pour la lecture.

 

Spécifie les flux qui ont été connectés correctement à un récepteur multimédia.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau de valeurs **DWORD** (**CAUL**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Remarques

Cette propriété peut être envoyée avec le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ Set** Event.

La valeur de la propriété est un tableau de **HRESULT** s. Les entrées de tableau correspondent aux flux sur l’élément multimédia actuel. Chaque entrée du tableau indique si le flux correspondant a été connecté à un récepteur multimédia, comme suit :

-   Si le flux est connecté à un récepteur multimédia, la valeur est **\_ OK**.
-   Si le flux n’est pas sélectionné, la valeur est **S \_ false**.
-   Si une erreur s’est produite lors de la tentative de connexion du flux, la valeur est un code d’erreur.

Si au moins un flux a été correctement connecté, la lecture est possible. Par exemple, l’utilisateur peut avoir le codec nécessaire pour lire le flux audio, mais pas pour lire le flux vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Mfplay. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_événement de \_ jeu de MEDIAITEM MFP \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




