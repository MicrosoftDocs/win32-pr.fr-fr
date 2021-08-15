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
ms.openlocfilehash: bd77019c98e48f4707ac173f825823d5637a1d83c5eb1583f4ee68874e84bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752700"
---
# <a name="ivmtaskwaitforcompletion-method"></a>IVMTask :: WaitForCompletion, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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



 

## <a name="remarks"></a>Remarques

La méthode **WaitForCompletion** met le thread d’exécution actuel en veille jusqu’à ce qu’il retourne. La spécification d’une attente infinie (timeout =-1) n’est pas recommandée, à moins qu’il soit absolument essentiel que la tâche se termine dans n’importe quelle circonstance.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

