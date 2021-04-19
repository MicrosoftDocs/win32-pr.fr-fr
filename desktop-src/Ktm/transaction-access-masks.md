---
description: KTM définit les masques d’accès aux transactions suivants à utiliser lors de l’ouverture d’une transaction.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Masques d’accès aux transactions (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518656"
---
# <a name="transaction-access-masks"></a>Masques d’accès aux transactions

KTM définit les masques d’accès aux transactions suivants à utiliser lors de l’ouverture d’une transaction.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_informations sur les requêtes de transaction \_**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



L’appelant peut interroger les informations de transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_ \_ informations sur le document informatisé**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



L’appelant peut définir des informations de transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**inscription des transactions \_**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



L’appelant peut s’inscrire dans cette transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**validation de TRANSACTION \_**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



L’appelant peut valider cette transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**restauration de TRANSACTION \_**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



L’appelant peut restaurer cette transaction.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**propagation de la TRANSACTION \_**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



L’appelant peut propager cette transaction à un gestionnaire de ressources supérieur, tel que le Distributed Transaction Coordinator (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_lecture générique de la transaction \_**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



L’appelant dispose des privilèges suivants : **\_ \_ lecture des droits standard**, **\_ \_ informations sur la requête de transaction** et **synchroniser**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_écriture générique de transaction \_**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



L’appelant dispose des privilèges suivants : **\_ \_ écriture des droits standard**, **\_ \_ informations sur** le document informatisé, **\_ validation** de la transaction, **\_ inscription** des transactions, **\_ restauration** de la transaction, **\_ propagation** de la transaction et **synchronisation**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_Exécution générique de la transaction \_**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



L’appelant dispose des privilèges suivants : **les \_ droits standard \_ s’exécutent**, la **\_ validation** de la transaction, la **\_ restauration** de la transaction et la **synchronisation**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_tout \_ accès aux transactions**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



L’appelant dispose des privilèges suivants : **\_ droits standard \_ requis**, **\_ \_ lecture générique de transaction**, **\_ \_ écriture générique** de transaction **et \_ \_ Exécution générique de transaction**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_droits du \_ Gestionnaire de ressources de transaction \_**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



L’appelant dispose des privilèges suivants : **\_ \_ lecture générique** de la transaction, **\_ \_ écriture des droits standard**, **\_ \_ informations sur** le document informatisé, **\_ restauration** de la transaction, **\_ inscription** des transactions, **\_ propagation** de la transaction et **synchroniser**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Il est recommandé que les gestionnaires de ressources, lors de l’inscription dans une transaction, spécifient les droits du gestionnaire de ressources de transaction lors de l’ouverture d’une transaction. **\_ \_ \_**

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




