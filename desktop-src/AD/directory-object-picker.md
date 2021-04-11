---
title: Sélecteur d’objets d’annuaire
description: La boîte de dialogue Sélecteur d’objets d’annuaire permet à un utilisateur de sélectionner un ou plusieurs objets à partir du catalogue global, d’un domaine ou d’un ordinateur ou d’un groupe de travail.
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- Active Directory Object Picker AD
- sélecteur d’objet AD
- objets AD, sélecteur d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6ba7fd053aa8ab3245bf72c693f0a887aa983
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031017"
---
# <a name="directory-object-picker"></a>Sélecteur d’objets d’annuaire

La boîte de dialogue Sélecteur d’objets d’annuaire permet à un utilisateur de sélectionner un ou plusieurs objets à partir du catalogue global, d’un domaine ou d’un ordinateur ou d’un groupe de travail. Les types d’objets à partir desquels un utilisateur peut sélectionner incluent les objets d’utilisateur, de contact, de groupe et d’ordinateur. Pour plus d’informations sur Active Directory Domain Services, consultez [Active Directory Domain Services](active-directory-domain-services.md).

Pour afficher une boîte de dialogue Sélecteur d’objets :

1.  Appelez la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) pour créer une instance de l’interface [**IDsObjectPicker**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker) .
2.  Appelez la méthode [**IDsObjectPicker :: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) pour initialiser la boîte de dialogue.
3.  Appelez la méthode [**IDsObjectPicker :: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) pour afficher la boîte de dialogue.
4.  Appelez la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de l’instance [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) renvoyée par la boîte de dialogue Sélecteur d’objets pour récupérer les données de la [**\_ \_ \_ \_ liste de sélection CFSTR DSOP DS**](cfstr-dsop-ds-selection-list.md) . Le format de presse-papiers de la **\_ \_ \_ \_ liste de sélection DS CFSTR DSOP** fournit un **HGLOBAL** qui contient une structure de [**\_ \_ liste de sélection des services d’annuaire**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . La structure de la **\_ \_ liste de sélection des services d’annuaire** contient des données sur les éléments sélectionnés dans la boîte de dialogue Sélecteur d’objets.

Si l’identificateur de sécurité (SID) est requis pour un objet, celui-ci doit être demandé directement à partir du sélecteur d’objets en ajoutant l’attribut **objectSID** à la liste d’attributs à récupérer pour l’objet sélectionné. La transmission du nom d’objet retourné à la fonction [**LsaLookupNames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) ou [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) n’est pas recommandée, car la recherche de nom sera redondante et risque d’échouer dans certains cas.

Si une référence à des objets sélectionnés est enregistrée, le nom unique ne doit pas être enregistré, car l’objet peut être déplacé, renommé ou peut être modifié en raison de différences de paramètres régionaux. Pour les principaux de sécurité, l' **objectSID** doit être demandé pour l’objet et enregistré en toute sécurité. Si le nom du principal de sécurité est nécessaire ultérieurement, il peut être récupéré avec la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . Pour tous les autres objets, l' **objectGUID** doit être demandé et enregistré.

## <a name="initialization"></a>Initialisation

Quand la boîte de dialogue Sélecteur d’objets est initialisée, un ensemble de types et de filtres d’étendue est spécifié. Les types d’étendues spécifiés déterminent, par exemple, les emplacements, les domaines ou les ordinateurs à partir desquels un utilisateur peut sélectionner des objets. Les filtres déterminent les types d’objets qu’un utilisateur peut sélectionner à partir d’un type d’étendue donné. Pour plus d’informations, consultez la section étendues et filtres ci-dessous.

Par défaut, un utilisateur peut sélectionner un seul objet dans la boîte de dialogue Sélecteur d’objets d’annuaire. Pour activer plusieurs sélections, définissez l’indicateur de **\_ \_ multisélection DSOP Flag** dans le membre **flOptions** de la structure d' [**\_ \_ informations init DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) lorsque la boîte de dialogue est initialisée.

## <a name="scopes-and-filters"></a>Étendues et filtres

La liste déroulante **regarder dans** contient les étendues à partir desquelles un utilisateur peut sélectionner des objets. Une étendue est un domaine, un ordinateur, un groupe de travail ou un catalogue global qui stocke des données sur un ensemble d’objets disponibles et permet d’y accéder. Les entrées de la liste étendue dépendent des types d’étendue et de l’ordinateur cible spécifié lors du dernier appel de la méthode [**IDsObjectPicker :: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) pour initialiser la boîte de dialogue Sélecteur d’objets.

Un type d’étendue est une catégorie générique d’étendues, telles que tous les domaines de l’entreprise à laquelle l’ordinateur cible appartient, ou le catalogue global pour l’entreprise de l’ordinateur cible, ou l’ordinateur cible lui-même. Pour chaque type d’étendue spécifié, la boîte de dialogue utilise le contexte de l’ordinateur cible pour déterminer les entrées de la liste d’étendues.

La méthode [**IDsObjectPicker :: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) accepte un pointeur vers une structure [**d' \_ \_ informations d’initialisation DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) qui contient un tableau de structures d' [**\_ \_ \_ informations init de portée DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) . Chaque entrée du tableau **d' \_ \_ \_ informations d’initialisation de l’étendue DSOP** spécifie un ou plusieurs types d’étendue, ainsi que les filtres applicables et d’autres attributs. Les filtres déterminent les types d’objets, tels que les utilisateurs, les groupes, les contacts et les ordinateurs, que l’utilisateur peut sélectionner à partir d’un type d’étendue donné. Lorsque l’utilisateur sélectionne une étendue dans la liste, la boîte de dialogue applique les filtres de ce type d’étendue pour afficher la liste des objets que l’utilisateur peut sélectionner.

Chaque structure d' [**\_ informations d' \_ initialisation \_ de portée DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) contient une structure d' [**\_ \_ indicateurs de filtre DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) qui spécifie les filtres pour ce type d’étendue. La structure d' **\_ \_ indicateurs de filtre DSOP** distingue les étendues de niveau supérieur et de niveau supérieur :

-   Une étendue de niveau supérieur est un catalogue global ou un domaine qui prend en charge le [fournisseur LDAP](/windows/desktop/ADSI/adsi-ldap-provider)ADSI.
-   Une étendue de niveau supérieur comprend des groupes de travail et tous les ordinateurs individuels. La boîte de dialogue utilise le fournisseur ADSI WinNT pour accéder à une étendue de niveau supérieur.

Deux ensembles d’indicateurs de filtre sont définis pour être utilisés dans la structure d' [**\_ \_ indicateurs de filtre DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) : un pour les portées de niveau supérieur et un pour les étendues de niveau inférieure. Le membre de **niveau supérieur** de la structure d' **\_ \_ indicateurs de filtre DSOP** est une structure d' [**indicateurs de \_ \_ filtre \_ de niveau supérieur DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags) qui spécifie les filtres pour les portées de niveau supérieur. Le membre **flDownlevel** de la structure d' **\_ \_ indicateurs de filtre DSOP** est un ensemble d’indicateurs qui spécifient les filtres pour les portées de niveau inférieure.

 

 