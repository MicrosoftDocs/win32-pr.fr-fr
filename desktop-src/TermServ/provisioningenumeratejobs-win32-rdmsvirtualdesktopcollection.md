---
title: Méthode ProvisioningEnumerateJobs de la classe Win32_RDMSVirtualDesktopCollection
description: Énumère les tâches de provisionnement de bureau virtuel pour ce service.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningEnumerateJobs
- Services Bureau à distance de la méthode ProvisioningEnumerateJobs, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008603"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Méthode ProvisioningEnumerateJobs de la \_ classe Win32 RDMSVirtualDesktopCollection

Énumère les tâches de provisionnement de bureau virtuel pour ce service.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*JobType* \[ dans\]
</dt> <dd>

Entier qui spécifie le type de travail à énumérer.

Ce paramètre peut être défini sur l’une des valeurs suivantes :

<dt>

0
</dt> <dd>

Travaux en cours d’exécution

</dd> <dt>

1
</dt> <dd>

Travaux terminés

</dd> </dl> </dd> <dt>

*CollectionAlias* \[ dans\]
</dt> <dd>

Alias de la collection de bureaux virtuels à énumérer. La valeur par défaut de ce paramètre est FALSe, ce qui indique que tous les travaux en cours d’exécution doivent être énumérés.

</dd> <dt>

*JobGuids* \[ à\]
</dt> <dd>

Tableau qui contient les **GUID** des tâches d’approvisionnement à énumérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





