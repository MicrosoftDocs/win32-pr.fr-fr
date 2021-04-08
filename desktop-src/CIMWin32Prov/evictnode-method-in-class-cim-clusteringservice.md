---
description: La méthode EvictNode supprime un système informatique d’un cluster. Le nœud à supprimer est spécifié en tant que paramètre de la méthode.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Méthode EvictNode de la classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748140"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a>Méthode EvictNode de la \_ classe CIM ClusteringService

La méthode **EvictNode** supprime un système informatique d’un cluster. Le nœud à supprimer est spécifié en tant que paramètre de la méthode.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CS* \[ dans\]
</dt> <dd>

Référence au système informatique à supprimer du cluster.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 (zéro) si le système informatique est correctement expulsé, 1 (un) si la méthode n’est pas prise en charge, et tout autre nombre si une erreur s’est produite.

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CLUSTERINGSERVICE CIM**](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> </dl>

 

