---
title: Message HKM_SETRULES (commctrl. h)
description: Définit les combinaisons non valides et la combinaison de modificateur par défaut pour un contrôle de touche d’accès rapide.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES les contrôles de Windows de message
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
ms.openlocfilehash: 4ec47450ca0d67854d7be413d8a3eb3e5fec3eac49e18f6bcf96f86b563c8906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958708"
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

## <a name="remarks"></a>Remarques

Lorsqu’un utilisateur entre une combinaison de touches non valide, comme défini par les indicateurs spécifiés dans *wParam*, le système utilise l’opérateur or au niveau du bit pour combiner les clés entrées par l’utilisateur avec les indicateurs spécifiés dans *lParam*. La combinaison de touches obtenue est convertie en chaîne, puis affichée dans le contrôle de touche d’accès rapide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





