---
description: KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture des enlistes.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Masques d’accès d’inscription (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f3d774c474c27896c16bba5c7552713f248519aa86ef56da0da5b704234b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870109"
---
# <a name="enlistment-access-masks"></a>Masques d’accès d’inscription

KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture des enlistes.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_informations sur la requête d’inscription \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



L’appelant peut interroger KTM pour obtenir des informations sur l’inscription.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_informations sur l’inscription \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



L’appelant peut définir des informations sur l’inscription.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**récupération de l’inscription \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



L’appelant peut récupérer une inscription.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**droits d’inscription \_ subordonnés \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



L’appelant peut effectuer les actions effectuées par un gestionnaire de ressources pour le compte de la transaction. Voici une liste d’actions :

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_droits supérieurs d’inscription \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



L’appelant peut s’inscrire dans la transaction en tant que gestionnaire de transactions supérieur.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_lecture générique d’inscription \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



L’appelant dispose des privilèges suivants : **informations standard \_ \_ sur les requêtes** de **\_ \_ lecture** et d’inscription.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_écriture générique d’inscription \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



L’appelant dispose des privilèges suivants : **l' \_ \_ écriture des droits standard**, les **\_ \_ informations du jeu d’inscription** et la **\_ récupération** de l’inscription.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_Exécution générique d’inscription \_**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



L’appelant dispose des privilèges suivants : autorisations **standard, \_ \_ exécution** de **\_ récupération d’inscription** et **\_ \_ droits subordonnés d’inscription**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**INSCRIPTION de \_ tous les \_ accès**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Cette valeur définit tous les bits valides pour une valeur d’accès d’inscription.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




