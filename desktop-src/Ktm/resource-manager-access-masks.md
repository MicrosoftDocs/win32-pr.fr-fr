---
description: KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de ressources.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Masques d’accès Gestionnaire des ressources (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ede54d5d49533e70aa9cda2d9c4a363d61f1fdbd894108a5b83f2c5e9efc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146482"
---
# <a name="resource-manager-access-masks"></a>Masques d’accès Gestionnaire des ressources

KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de ressources.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_informations sur les requêtes RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



L’appelant peut demander des informations sur le gestionnaire de ressources (RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_informations sur l’ensemble de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



L’appelant peut définir les informations du gestionnaire de configuration.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**Recover RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



L’appelant peut récupérer le RM spécifié.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**inscription de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



L’appelant peut inscrire un RM dans une transaction.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**NOTIFICATION d’accès à RESOURCEMANAGER \_ \_**
</dt> <dd> <dl> <dt>



L’appelant peut recevoir une notification pour un RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_lecture générique \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



L’appelant dispose des privilèges suivants : \_ lecture des droits standard \_ , \_ \_ informations sur les requêtes RESOURCEMANAGER et \_ recover ResourceManager.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_écriture générique \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



L’appelant dispose des privilèges suivants : \_ écriture des droits standard \_ , \_ \_ informations sur le jeu de données, inscription ResourceManager et notification d’accès à \_ ResourceManager \_ \_ .


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_Exécution générique \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



L’appelant dispose des privilèges suivants : \_ droits d' \_ exécution standard, \_ inscription ResourceManager et \_ \_ notification d’accès à ResourceManager.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_tout \_ accès à RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



L’appelant dispose des privilèges suivants : \_ droits standard \_ requis.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




