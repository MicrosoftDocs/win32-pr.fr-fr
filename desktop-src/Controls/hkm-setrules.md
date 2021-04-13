---
title: Message HKM_SETRULES (commctrl. h)
description: Définit les combinaisons non valides et la combinaison de modificateur par défaut pour un contrôle de touche d’accès rapide.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES les contrôles de message Windows
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465694"
---
# <a name="hkm_setrules-message"></a>\_Message hkm SETRULES

Définit les combinaisons non valides et la combinaison de modificateur par défaut pour un contrôle de touche d’accès rapide.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Tableau d’indicateurs qui spécifient des combinaisons de touches non valides. Ce paramètre peut être une combinaison des valeurs suivantes :



| Valeur                                                                                                                                                   | Signification                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | Alt<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**\_autorité de certification HKCOMB**</dt> </dl>       | CTRL + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ aucun**</dt> </dl> | Clés non modifiées<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | MAJUSCULE<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**HKCOMB \_ sa**</dt> </dl>       | Maj+Alt<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | MAJ + CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | MAJ + CTRL + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Tableau d’indicateurs qui spécifient la combinaison de touches à utiliser lorsque l’utilisateur entre une combinaison non valide. Pour obtenir la liste des valeurs d’indicateur de modification, consultez la description du message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Lorsqu’un utilisateur entre une combinaison de touches non valide, comme défini par les indicateurs spécifiés dans *wParam*, le système utilise l’opérateur or au niveau du bit pour combiner les clés entrées par l’utilisateur avec les indicateurs spécifiés dans *lParam*. La combinaison de touches obtenue est convertie en chaîne, puis affichée dans le contrôle de touche d’accès rapide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





