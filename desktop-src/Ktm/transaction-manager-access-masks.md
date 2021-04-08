---
description: KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de transactions (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Masques d’accès du gestionnaire de transactions (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864566"
---
# <a name="transaction-manager-access-masks"></a>Masques d’accès du gestionnaire de transactions

KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de transactions (TM).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_informations sur les requêtes TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



L’appelant peut demander des informations sur ce TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_informations sur l’ensemble de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



L’appelant peut définir des informations sur ce TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**récupération de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



L’appelant peut récupérer ce TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**renommer TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



L’appelant peut renommer une instance de TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ créer \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



L’appelant peut créer un gestionnaire de ressources associé à ce TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_transaction de liaison TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Cette valeur est réservée.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_lecture générique \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



L’appelant dispose des privilèges suivants : **\_ droits standard \_ lecture** et **\_ \_ informations sur les requêtes TRANSACTIONMANAGER**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_écriture générique \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



L’appelant dispose des privilèges suivants : **\_ \_ écriture des droits standard**, **\_ \_ informations sur le jeu de TRANSACTIONMANAGER**, **\_ récupération de TransactionManager**, **\_ renommage** de l’ensemble de données et **TransactionManager \_ créer \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_Exécution générique de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



L’appelant dispose des privilèges suivants : **les \_ droits standard \_ s’exécutent**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**\_tout \_ accès à TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Cette valeur définit tous les bits valides pour une valeur d’accès TM.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




