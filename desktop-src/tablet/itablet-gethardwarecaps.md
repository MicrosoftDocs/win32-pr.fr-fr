---
description: Retourne une valeur qui représente les fonctionnalités du matériel de tablette.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'ITablet :: GetHardwareCaps, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523173"
---
# <a name="itabletgethardwarecaps-method"></a>ITablet :: GetHardwareCaps, méthode

Retourne une valeur qui représente les fonctionnalités du matériel de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwCaps* \[ à\]
</dt> <dd>

Indicateurs binaires qui représentent les fonctionnalités du matériel de tablette.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Le paramètre *pdwCaps* est un jeu d’indicateurs binaires qui décrivent les fonctionnalités matérielles de Tablet PC. Le tableau suivant décrit ces indicateurs.



| Nom de l’indicateur                         | Valeur                 | Description                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| THWC \_ intégré<br/>       | 0x00000001<br/> | Indique que l’affichage et le digitaliseur partagent la même surface.<br/>                                                    |
| THWC \_ CSR \_ doit \_ toucher<br/> | 0x00000002<br/> | Indique que le curseur doit être dans un contact physique avec l’appareil pour signaler la position.<br/>                           |
| \_proximité THWC \_<br/>  | 0x00000004<br/> | Indique que l’appareil peut générer des événements lorsque le curseur entre en entrée et en quittant la plage de détection physique.<br/> |
| THWC \_ PHYSID \_ CSR<br/>     | 0x00000008<br/> | Indique que l’appareil peut identifier de manière unique le curseur actif dans le matériel.<br/>                                      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




