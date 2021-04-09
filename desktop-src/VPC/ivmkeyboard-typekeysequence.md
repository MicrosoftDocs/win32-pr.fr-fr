---
title: Méthode IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simule une liste délimitée par des virgules des clés en cours de saisie.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Méthode TypeKeySequence Virtual PC
- Méthode TypeKeySequence Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, méthode TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942782"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>IVMKeyboard :: TypeKeySequence, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simule une liste délimitée par des virgules des clés en cours de saisie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*séquence de touches* \[ dans\]
</dt> <dd>

Séquence de codes clés délimités par des virgules à taper.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                   |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | La chaîne spécifiée est vide ou contient un code de clé non valide.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                               |



 

## <a name="remarks"></a>Notes

Une chaîne de séquence clé est un ensemble d’identificateurs de clé délimités par des virgules, qui sont utilisés pour simuler l’appui sur la touche et la séquence de mise en version d’un clavier standard de style « 101 ».

Si un identificateur de clé apparaît dans la chaîne sans modificateur précédent, un code appuyé sur la touche est envoyé à la session de l’ordinateur virtuel, suivi immédiatement du code de sortie de la clé correspondant. Les modificateurs de clé peuvent être utilisés pour modifier ce comportement.

Par exemple, le modificateur UpDown envoie le code appuyé sur la touche pour l’identificateur de clé suivant sans envoyer le code de sortie de clé. Cela est utile pour simuler les touches Ctrl, Alt et Maj lorsqu’elles sont maintenues pendant que d’autres touches sont envoyées. Pour libérer la clé, elle doit être incluse dans la chaîne de clé avec un modificateur UP précédent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> <dt>

[Séquences de touches](key-sequences.md)
</dt> </dl>

 

