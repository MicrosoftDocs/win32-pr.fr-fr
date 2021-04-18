---
description: Spécifie les flux qui ont été connectés correctement à un récepteur multimédia.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: MFP_PKEY_StreamRenderingResults, propriété (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318546"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>\_Propriété StreamRenderingResults de la propriété HYPERmfp \_

> [!IMPORTANT]
> Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows. Les applications doivent utiliser la [session multimédia](media-session.md) pour la lecture.

 

Spécifie les flux qui ont été connectés correctement à un récepteur multimédia.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau de valeurs **DWORD** (**CAUL**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Notes

Cette propriété peut être envoyée avec le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ Set** Event.

La valeur de la propriété est un tableau de **HRESULT** s. Les entrées de tableau correspondent aux flux sur l’élément multimédia actuel. Chaque entrée du tableau indique si le flux correspondant a été connecté à un récepteur multimédia, comme suit :

-   Si le flux est connecté à un récepteur multimédia, la valeur est **\_ OK**.
-   Si le flux n’est pas sélectionné, la valeur est **S \_ false**.
-   Si une erreur s’est produite lors de la tentative de connexion du flux, la valeur est un code d’erreur.

Si au moins un flux a été correctement connecté, la lecture est possible. Par exemple, l’utilisateur peut avoir le codec nécessaire pour lire le flux audio, mais pas pour lire le flux vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Mfplay. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_événement de \_ jeu de MEDIAITEM MFP \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




