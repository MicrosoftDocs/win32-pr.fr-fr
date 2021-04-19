---
title: Méthode IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Attend que la tâche soit terminée ou que l’intervalle de délai d’attente spécifié soit écoulé.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Méthode WaitForCompletion Virtual PC
- Méthode WaitForCompletion Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, méthode WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510765"
---
# <a name="ivmtaskwaitforcompletion-method"></a>IVMTask :: WaitForCompletion, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attend que la tâche soit terminée ou que l’intervalle de délai d’attente spécifié soit écoulé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*délai d’expiration* \[ dans\]
</dt> <dd>

Durée, en millisecondes, pendant laquelle cette méthode attendra la fin de l’exécution de la tâche avant de retourner le contrôle à l’appelant. Une valeur de-1 spécifie que la méthode attendra jusqu’à ce que la tâche se termine sans dépasser le délai d’attente. Les autres valeurs valides de délai d’attente sont comprises entre 0 et 4 millions millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | Le paramètre de *délai d’attente* n’est pas valide.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>     |



 

## <a name="remarks"></a>Notes

La méthode **WaitForCompletion** met le thread d’exécution actuel en veille jusqu’à ce qu’il retourne. La spécification d’une attente infinie (timeout =-1) n’est pas recommandée, à moins qu’il soit absolument essentiel que la tâche se termine dans n’importe quelle circonstance.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

