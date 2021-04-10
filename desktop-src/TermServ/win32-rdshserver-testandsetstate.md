---
title: Méthode TestAndSetState de la classe Win32_RDSHServer
description: Compare l’état actuel à l’objet comparand spécifié ; Si les deux correspondent, l’État est défini sur une nouvelle valeur. Quelle que soit la correspondance, l’état actuel est également retourné.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TestAndSetState
- Services Bureau à distance de la méthode TestAndSetState, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103984"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a>Méthode TestAndSetState de la \_ classe Win32 RDSHServer

Compare l’état actuel à l’objet comparand spécifié ; Si les deux correspondent, l’État est défini sur une nouvelle valeur. Quelle que soit la correspondance, l’état actuel est également retourné.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Comparand* \[ dans\]
</dt> <dd>

Valeur à comparer à l’état actuel. Si les deux valeurs correspondent, l’État est défini sur *NewState*.

</dd> <dt>

*NewState* \[ dans\]
</dt> <dd>

Nouvelle valeur de l’État.

</dd> <dt>

*InitState* \[ à\]
</dt> <dd>

En cas de réussite ou d’échec, retourne l’état actuel.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





