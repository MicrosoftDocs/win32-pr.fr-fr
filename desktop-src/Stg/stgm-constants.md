---
title: Constantes STGM (ObjBase. h)
description: Indicateurs qui indiquent des conditions pour la création et la suppression des objets et des modes d’accès pour l’objet.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18248e862c3d5981e9c34b29522b1cd75d2b61cf78a52613b3d28a1d2c98b4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661969"
---
# <a name="stgm-constants"></a>Constantes STGM

Les constantes STGM sont des indicateurs qui indiquent des conditions pour la création et la suppression des modes d’accès et d’objet pour l’objet. Les constantes STGM sont incluses dans les interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et dans les fonctions [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)et [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .

Ces éléments sont souvent combinés à l’aide d’un opérateur **or**. Elles sont interprétées dans des groupes répertoriés dans le tableau suivant. L’utilisation de plusieurs éléments à partir d’un seul groupe n’est pas valide.

Utilisez un indicateur du groupe de création lors de la création d’un objet, par exemple avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).

Pour plus d’informations sur les transactions, consultez la section Notes.



| Groupe                      | Indicateur                         | Valeur       |
|----------------------------|------------------------------|-------------|
| Accès                     | **\_lecture STGM**               | 0x00000000L |
|                            | **\_écriture STGM**              | 0x00000001L |
|                            | **STGM \_ ReadWrite**          | 0x00000002L |
| Partage                    | **\_partage STGM \_ Deny \_ None**  | 0x00000040L |
|                            | **\_ \_ lecture refusée du partage STGM \_**  | 0x00000030L |
|                            | **\_partage STGM \_ refuser l' \_ écriture** | 0x00000020L |
|                            | **\_partage STGM \_ exclusif**   | 0x00000010L |
|                            | **\_priorité STGM**           | 0x00040000L |
| Création                   | **STGM \_ créer**             | 0x00001000L |
|                            | **STGM \_ convertir**            | 0x00020000L |
|                            | **STGM \_ FAILIFTHERE**        | 0x00000000L |
| Transactions             | **STGM \_ direct**             | 0x00000000L |
|                            | **STGM \_ traité**         | 0x00010000L |
| Performances des transactions | **STGM \_ NOrayer**          | 0x00100000L |
|                            | **STGM \_ NOsnapshot**         | 0x00200000L |
| SWMR directe et simple     | **STGM \_ simple**             | 0x08000000L |
|                            | **STGM \_ direct \_ SWMR**       | 0x00400000L |
| Supprimer au lancement          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**\_lecture STGM**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indique que l’objet est en lecture seule, ce qui signifie que les modifications ne peuvent pas être effectuées. Par exemple, si un objet de flux est ouvert avec **STGM \_ Read**, la méthode [**ISequentialStream :: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) peut être appelée, mais la méthode [**ISequentialStream :: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) peut ne pas l’être. De même, si un objet de stockage ouvert avec **STGM est \_ lu**, les méthodes [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) et [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) peuvent être appelées, mais les méthodes [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) et [**IStorage :: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) peuvent ne pas l’être.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**\_écriture STGM**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Vous permet d’enregistrer les modifications apportées à l’objet, mais n’autorise pas l’accès à ses données. Les implémentations fournies des interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ne prennent pas en charge ce mode en écriture seule.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ ReadWrite**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Active l’accès et la modification des données d’objet. Par exemple, si un objet de flux est créé ou ouvert dans ce mode, il est possible d’appeler à la fois [**IStream :: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) et **IStream :: Write**. N’oubliez pas que cette constante n’est pas un simple fichier binaire **ou** une opération des éléments de **\_ lecture** **STGM \_ Write** et STGM.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**\_partage STGM \_ Deny \_ None**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Spécifie que l’accès en lecture ou en écriture n’est pas refusé aux ouvertures suivantes de l’objet. Si aucun indicateur du groupe de partage n’est spécifié, cet indicateur est supposé.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**\_ \_ lecture refusée du partage STGM \_**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Empêche d’autres utilisateurs d’ouvrir l’objet en mode de **\_ lecture STGM** . Il est généralement utilisé sur un objet de stockage racine.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**\_partage STGM \_ refuser l' \_ écriture**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Empêche d’autres utilisateurs d’ouvrir l’objet pour **STGM \_ Write** ou **STGM \_ ReadWrite** Access. En mode traité, le partage d’un partage **STGM \_ \_ Deny \_** de partage d’écriture ou de partage STGM peut améliorer les performances de manière significative, car il ne requiert pas d’instantanés. **\_ \_** Pour plus d’informations sur les transactions, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**\_partage STGM \_ exclusif**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Empêche d’autres utilisateurs d’ouvrir l’objet dans n’importe quel mode. N’oubliez pas que cette valeur n’est pas une **opération de bits or simple** du **partage STGM refuser les valeurs d’écriture de refus de \_ \_ \_ lecture** et de **\_ partage \_ \_ STGM** . En mode traité, le partage d’un partage **STGM \_ \_ Deny \_** de partage d’écriture ou de partage STGM peut améliorer les performances de manière significative, car il ne requiert pas d’instantanés. **\_ \_** Pour plus d’informations sur les transactions, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_priorité STGM**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Ouvre l’objet de stockage avec un accès exclusif à la version la plus récemment validée. Ainsi, les autres utilisateurs ne peuvent pas valider les modifications apportées à l’objet tant qu’il est ouvert en mode de priorité. Vous obtenez des avantages en matière de performances pour les opérations de copie, mais vous empêchez les autres de valider les modifications. Limitez le temps pendant lequel les objets sont ouverts en mode de priorité. Vous devez spécifier **STGM \_ direct** et **STGM \_ Read** with Priority (mode de priorité) et vous ne pouvez pas spécifier **STGM \_ DELETEONRELEASE**. **STGM \_ DELETEONRELEASE** est valide uniquement lors de la création d’un objet racine, par exemple avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Elle n’est pas valide lors de l’ouverture d’un objet racine existant, par exemple avec [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex). Elle n’est pas non plus valide lors de la création ou de l’ouverture d’un sous-élément, par exemple, avec [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ créer**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Indique qu’un flux ou un objet de stockage existant doit être supprimé avant que le nouvel objet ne le remplace. Un nouvel objet est créé lorsque cet indicateur est spécifié uniquement si l’objet existant a été supprimé avec succès.

Cet indicateur est utilisé lors de la tentative de création de :

-   Un objet de stockage sur un disque, mais il existe un fichier portant ce nom.
-   Objet à l’intérieur d’un objet de stockage, mais il existe un objet portant le nom spécifié.
-   Objet de tableau d’octets, mais avec le nom spécifié existe.

Cet indicateur ne peut pas être utilisé avec des opérations d’ouverture, telles que [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ou [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ convertir**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Crée le nouvel objet tout en conservant les données existantes dans un flux nommé « contents ». Dans le cas d’un objet de stockage ou d’un tableau d’octets, les anciennes données sont mises en forme dans un flux, que le fichier ou le tableau d’octets existant contient actuellement un objet de stockage en couches. Cet indicateur ne peut être utilisé que lors de la création d’un objet de stockage racine. Elle ne peut pas être utilisée dans un objet de stockage ; par exemple, dans [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Il n’est pas non plus valide d’utiliser cet indicateur et l’indicateur **STGM \_ DELETEONRELEASE** simultanément.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Provoque l’échec de l’opération de création si un objet existant portant le nom spécifié existe. Dans ce cas, **STG \_ E \_ FILEALREADYEXISTS** est retourné. Il s’agit du mode de création par défaut ; autrement dit, si aucun autre indicateur Create n’est spécifié, **STGM \_ FAILIFTHERE** est implicite.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ direct**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indique que, en mode direct, chaque modification apportée à un élément de stockage ou de flux est écrite telle qu’elle se produit. Il s’agit de la valeur par défaut si aucune **STGM \_ directe** ni **STGM \_ traitée** n’est spécifiée.


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ traité**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Indique que, en mode traité, les modifications sont mises en mémoire tampon et écrites uniquement si une opération de validation explicite est appelée. Pour ignorer les modifications, appelez la méthode [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) dans l’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)ou [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . L’implémentation de fichier composé COM de **IStorage** ne prend pas en charge les flux transactionnels, ce qui signifie que les flux ne peuvent être ouverts qu’en mode direct, et que vous ne pouvez pas annuler les modifications apportées, mais les stockages transactionnels sont pris en charge. Les implémentations de fichiers composés, autonomes et de système de fichiers NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ne prennent pas en charge les jeux de propriétés transactionnels, simples, car ces jeux de propriétés sont stockés dans des flux. Toutefois, les transactions de jeux de propriétés qui peuvent être créés en spécifiant l’indicateur **PROPSETFLAG not \_ simple** dans le paramètre *grfFlags* de [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), sont prises en charge.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOrayer**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Indique que, en mode traité, un fichier de travail temporaire est généralement utilisé pour enregistrer les modifications jusqu’à ce que la méthode de **validation** soit appelée. La spécification de **STGM \_ noscratch** permet d’utiliser la partie inutilisée du fichier d’origine comme espace de travail au lieu de créer un fichier à cet effet. Cela n’affecte pas les données dans le fichier d’origine et, dans certains cas, les performances peuvent être améliorées. Il n’est pas possible de spécifier cet indicateur sans spécifier également **STGM \_ traité**, et cet indicateur ne peut être utilisé que dans une racine ouverte. Pour plus d’informations sur le mode noscratch, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Cet indicateur est utilisé lors de l’ouverture d’un objet de stockage avec **STGM \_** et sans **\_ partage STGM partage \_ exclusif** ou **partage de STGM refus d' \_ \_ \_ écriture**. Dans ce cas, la spécification de **STGM \_ nosnapshot** empêche l’implémentation fournie par le système de créer une copie d’instantané du fichier. Au lieu de cela, les modifications apportées au fichier sont écrites à la fin du fichier. L’espace inutilisé n’est pas récupéré à moins que la consolidation ne soit effectuée pendant la validation et qu’il n’y ait qu’un seul writer en cours sur le fichier. Lorsque le fichier est ouvert en mode sans instantané, une autre opération d’ouverture ne peut pas être effectuée sans spécifier **STGM \_ nosnapshot**. Cet indicateur ne peut être utilisé que dans une opération d’ouverture racine. Pour plus d’informations sur le mode nosnapshot, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ simple**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Fournit une implémentation plus rapide d’un fichier composé dans un cas limité, mais fréquemment utilisé. Pour plus d'informations, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ direct \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Prend en charge le mode direct pour les opérations de fichier multilecture et à rédacteur unique. Pour plus d'informations, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Indique que le fichier sous-jacent doit être détruit automatiquement lorsque l’objet de stockage racine est libéré. Cette fonctionnalité est particulièrement utile pour créer des fichiers temporaires. Cet indicateur ne peut être utilisé que lors de la création d’un objet racine, par exemple avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Elle n’est pas valide lors de l’ouverture d’un objet racine, par exemple avec [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), ou lors de la création ou de l’ouverture d’un sous-élément, par exemple, avec [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Il n’est pas non plus valide d’utiliser cet indicateur et l' \_ indicateur STGM Convert simultanément.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez combiner ces indicateurs, mais vous ne pouvez choisir qu’un seul indicateur de chaque groupe d’indicateurs associés. En général, un indicateur de chacun des groupes d’accès et de partage doit être spécifié pour toutes les fonctions et méthodes qui utilisent ces constantes. Les indicateurs d’autres groupes sont facultatifs.

### <a name="transacted-mode"></a>Mode traité

Lorsque l' **indicateur \_ direct STGM** est spécifié, une seule combinaison des indicateurs suivants peut être spécifiée à partir des groupes d’accès et de partage.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

N’oubliez pas que le mode direct est implicite en l’absence de **\_ transaction STGM**. Autrement dit, si aucune **STGM \_ directe** ni **STGM \_ traitée** n’est spécifiée, **STGM \_ direct** est supposé.

Lorsque l’indicateur **STGM \_ traité** est spécifié, les objets sont créés ou ouverts en mode traité. Dans ce mode, les modifications apportées à un objet ne sont pas conservées tant qu’elles ne sont pas validées. Par exemple, les modifications apportées à un objet de stockage transactionnel ne sont pas conservées tant que la méthode [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) n’est pas appelée. Les modifications apportées à un objet de stockage de ce type seront perdues si l’objet de stockage est libéré (version finale) avant l’appel de la méthode **Commit** ou si la méthode [**IStorage :: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) est appelée.

Lorsqu’un objet est créé ou ouvert en mode transactionnel, l’implémentation doit conserver les données d’origine et les mises à jour de ces données, afin que les mises à jour puissent être annulées si nécessaire. Cela s’effectue généralement en écrivant les modifications dans un espace de travail jusqu’à ce qu’elles soient validées, ou en créant une copie, appelée instantané, des données récemment validées.

Lorsqu’un objet de stockage racine est ouvert en mode transactionnel, l’emplacement et le comportement des données de travail et des copies d’instantanés peuvent être contrôlés pour optimiser les performances avec les indicateurs **STGM \_ noéraflure** et **STGM \_ nosnapshot** . (Un objet de stockage racine est obtenu à partir de, par exemple, la fonction [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ; un objet de stockage obtenu à partir de la méthode [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) est un objet de sous-stockage.) En règle générale, les captures instantanées et les données de travail sont stockées dans des fichiers temporaires, séparées du stockage.

L’effet de ces indicateurs dépend du nombre de lecteurs et/ou d’enregistreurs accédant au stockage racine.

Dans le cas d’un seul rédacteur, un objet de stockage en mode transactionnel est ouvert pour l’accès en écriture et il ne peut pas y avoir d’autre accès au fichier. Autrement dit, le fichier est ouvert avec **STGM \_ traité**, l’accès à **STGM \_ Write** ou **STGM \_ ReadWrite** et le partage du **\_ partage STGM share \_ exclusif**. Dans ce cas, les modifications apportées à l’objet de stockage sont écrites dans la zone Scratch. Lorsque ces modifications sont validées, elles sont copiées dans le stockage d’origine. Par conséquent, si aucune modification n’est apportée à l’objet de stockage, aucun transfert de données n’est nécessaire.

Dans le cas de « plusieurs rédacteurs », un objet de stockage traité est ouvert pour l’accès en écriture, mais il est partagé dans ce asway comme pour permettre à d’autres enregistreurs. Autrement dit, l’objet de stockage est ouvert **avec \_ STGM traité**, l’accès à **STGM \_ Write** ou **STGM \_ ReadWrite**, et le partage du **\_ partage STGM Deny est \_ \_ Read**. Si le partage **du \_ partage STGM \_ Deny \_ None** n’est pas spécifié, alors la casse est « multiple-Writer, multi-Reader ». Dans ce cas, une capture instantanée des données d’origine est effectuée pendant l’opération d’ouverture. Par conséquent, même si aucune modification n’est apportée au stockage et/ou qu’elle n’est pas réellement ouverte par un autre writer simultanément, le transfert de données est toujours nécessaire lors de l’ouverture. Par conséquent, il est possible d’obtenir les meilleures performances d’ouverture en ouvrant l’objet de stockage dans **STGM \_ partage \_ refuser l' \_ écriture** ou partager des STGM en mode **\_ \_ exclusif** . Pour plus d’informations sur la façon dont les modifications sont validées lorsqu’il y a plusieurs Writers, consultez [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

Dans le cas d’un « writer unique, à plusieurs lecteurs », un objet de stockage traité est ouvert pour l’accès en écriture, mais il est partagé avec les lecteurs. Autrement dit, l’objet de stockage est ouvert par l’enregistreur **avec \_ STGM traité**, l’accès à **STGM \_ ReadWrite** ou **STGM \_ Write**, et le partage du **\_ partage STGM refuse l' \_ \_ écriture**. Le stockage est ouvert par les lecteurs avec les **STGM \_ traités**, l’accès à **STGM \_ Read** et le partage du **\_ partage STGM \_ \_** ne sont pas associés. Dans ce cas, le writer utilise la zone Scratch pour stocker les modifications non validées. Comme dans les cas ci-dessus, le lecteur entraîne une pénalité de performance à l’heure d’ouverture pendant la création d’une copie d’instantané des données.

En règle générale, la zone Scratch est un fichier temporaire distinct des données d’origine. Lorsque des modifications sont validées dans le fichier d’origine, les données doivent être transférées à partir du fichier temporaire. Pour éviter ce transfert de données, l’indicateur **\_ noscratch STGM** peut être spécifié. Lorsque cet indicateur est spécifié, des parties du fichier d’objet de stockage sont utilisées pour la zone Scratch, plutôt que pour un fichier temporaire distinct. Par conséquent, la validation des modifications peut être effectuée rapidement, car un faible transfert de données est nécessaire. L’inconvénient est que le fichier de stockage peut devenir plus volumineux qu’il ne le serait, car il doit être augmenté pour être suffisamment grand pour les données d’origine et la zone de travail. Pour consolider les données et supprimer cette zone superflue, rouvrez le stockage racine en mode traité, mais sans définir l’indicateur **\_ noscratch STGM** . Ensuite, appelez [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) avec l' **indicateur \_ consolider STGC** défini.

La zone d’instantané, comme la zone Scratch, est également, en général, un fichier temporaire, ce qui peut aussi être affecté par un indicateur STGM. En spécifiant l’indicateur **STGM \_ nosnapshot** , un fichier d’instantané temporaire distinct n’est pas créé. Au lieu de cela, les données d’origine ne sont jamais modifiées, même s’il existe un ou plusieurs enregistreurs par objet. Lorsque des modifications sont validées, elles sont ajoutées au fichier, mais les données d’origine restent intactes. Ce mode augmente l’efficacité, car il réduit le temps d’exécution en éliminant la nécessité de créer un instantané lors de l’opération d’ouverture. Toutefois, l’utilisation de ce mode peut aboutir à un fichier de stockage très volumineux, car les données du fichier ne peuvent jamais être remplacées. Il n’y a aucune limite à la taille des fichiers ouverts en mode nosnapshot.

### <a name="direct-single-writer-multiple-reader-mode"></a>Mode de rédacteur direct, Multiple-Reader

Comme décrit, il est possible d’avoir un seul Writer et plusieurs lecteurs d’un objet de stockage, si cet objet est ouvert en mode traité. Il est également possible d’obtenir le cas d’un seul writer en mode direct, en spécifiant l’indicateur **STGM \_ direct \_ SWMR** .

En mode **STGM \_ direct \_ SWMR** , il est possible pour un appelant d’ouvrir un objet pour l’accès en lecture/écriture, tandis que d’autres appellent simultanément le fichier ouvert pour l’accès en lecture seule. L’utilisation de cet indicateur n’est pas valide en association avec l’indicateur **STGM \_ traité** . Dans ce mode, le writer ouvre l’objet avec les indicateurs suivants :

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ share \_ DENYWRITE**

et chacun des lecteurs ouvre l’objet avec les indicateurs suivants :

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ lire** \| **STGM \_ partager \_ refuser \_ aucun**

Dans ce mode, pour modifier l’objet de stockage, l’enregistreur doit bénéficier d’un accès exclusif à l’objet. Cela est possible lorsque tous les lecteurs l’ont fermé. Le writer utilise l’interface [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) pour obtenir cet accès exclusif.

### <a name="simple-mode"></a>Mode simple

Le mode simple (**STGM \_ simple**) est utile pour les applications qui effectuent des opérations de sauvegarde complètes. Elle est efficace, mais elle présente les contraintes suivantes :

-   Il n’existe aucune prise en charge pour les sous-stockages.
-   L’objet de stockage et les objets de flux obtenus à partir de celui-ci ne peuvent pas être marshalés.
-   Chaque flux a une taille minimale. Si le nombre minimal d’octets est écrit dans un flux lorsque le flux est libéré, le flux est étendu à la taille minimale. Par exemple, la taille minimale d’une implémentation [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) particulière est de 4 Ko. Un flux est créé et 1 Ko y est écrit. À la version finale de cet **IStream**, la taille du flux sera automatiquement étendue à 4 Ko. Par la suite, l’ouverture du flux et l’appel de la méthode [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) affichent une taille de 4 Ko.
-   Les méthodes de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ne seront pas toutes prises en charge par l’implémentation. Pour plus d’informations, consultez la rubrique relative [à l’implémentation d’un fichier composé IStorage](istorage-compound-file-implementation.md)et à l' [implémentation d’un fichier composé IStream](istream-compound-file-implementation.md).

Le [marshaling](/windows/desktop/Midl/marshaling-ole-data-types) est le processus d’empaquetage, de empaquetage et d’envoi de paramètres de méthode d’interface à travers des limites de thread ou de processus au sein d’un appel de procédure distante (RPC). Pour plus d’informations, consultez [Détails du marshaling](../com/marshaling-details.md) et [marshaling](../com/interface-marshaling.md)de l’interface.

Lorsqu’un objet de stockage est obtenu par une opération de création en mode simple :

-   Vous pouvez créer des éléments de flux, mais pas les ouvrir.
-   Lorsqu’un élément de flux est créé en appelant [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), il n’est pas possible de créer un autre flux tant que cet objet de flux n’est pas libéré.
-   Une fois tous les flux écrits, appelez [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) pour vider les modifications.

Lorsqu’un objet de stockage est obtenu par une opération d’ouverture en mode simple :

-   Il est possible d’ouvrir un seul élément de flux à la fois.
-   Il n’est pas possible de modifier la taille d’un flux en appelant la méthode [**IStream :: assets**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) ou en recherchant ou en écrivant au-delà de la fin du flux. Toutefois, étant donné que tous les flux ont une taille minimale, il est possible d’utiliser le flux jusqu’à cette taille, même si moins de données ont été écrites à l’origine. Pour déterminer la taille d’un flux, utilisez la méthode [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .

Sachez que, si un élément de stockage est modifié par un objet de stockage qui n’est pas en mode simple, il n’est pas possible, encore une fois, d’ouvrir cet élément de stockage en mode simple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ObjBase. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISequentialStream :: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

