---
title: Gestion des schémas
description: Le composant fournisseur d’exemples ADSI définit les classes de schéma \ 0034 ; unité d’organisation \ 0034 ; et \ 0034 ; Utilisateur \ 0034 ; et gère ces classes de schéma de la façon suivante.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Gestion des schémas (ADSI)
- gestion des schémas (ADSI)
- gestion des schémas ADSI
- schémas, gérer ADSI
- gestion d’un schéma ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddb8fcc3d29dce27ac2b74c9c8e79d1cef2f9d2a23307e9b7626861ed3e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770483"
---
# <a name="schema-management"></a>Gestion des schémas

Le composant fournisseur d’exemples ADSI définit les classes de schéma « unité d’organisation » et « utilisateur » et gère ces classes de schéma de la façon suivante.

La classe de schéma « unité d’organisation » est représentée par un objet conteneur ADs et peut contenir d’autres « unités organisationnelles » et « utilisateurs ». L’objet conteneur prend en charge les interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)et [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). La classe de schéma « User » est représentée par un objet Active Directory générique et ne contient pas d’autres types d’objets. Dans l’exemple de composant fournisseur, l’objet utilisateur est implémenté en tant qu’objet Active Directory générique qui prend en charge les interfaces **IUnknown**, **IDispatch** et **IADs**. N’oubliez pas que l’objet utilisateur, dans ce cas, ne prend pas en charge l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

L’exemple de composant de fournisseur doit également implémenter l’objet espace de noms ADs, qui prend en charge les interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)et [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

L’illustration suivante montre les détails du schéma qui représente les deux exemples de classes de schéma de composant fournisseur.

![schéma du composant fournisseur de l’exemple ADSI](images/dssmsch.png)

Notez que dans la figure précédente, la classe de schéma « unité d’organisation » définit trois propriétés : « description », « effectifs » et « ID ». La classe de schéma « User » définit quatre propriétés : « ID », « Name », « PhoneNumber » et « title ». La propriété « ID » est partagée par les deux classes de schéma. Chaque propriété est définie par l’objet de syntaxe « String » ou « Integer ».

> [!Note]  
> Les objets de syntaxe ne sont pas présents dans la première version de l’exemple de composant fournisseur. Toutefois, dans la plupart des implémentations de schéma Microsoft ADSI, les objets de syntaxe sont inclus dans l’objet de conteneur de schéma, tout comme les objets de classe et de propriété de schéma. Pour cette raison, elles s’affichent ici.

 

Ce composant de fournisseur rend les données de schéma accessibles à l’application cliente ADSI sous la forme d’objets de classe ADs, d’objets de propriété ADs et d’objets de syntaxe ADs, le tout au sein d’un objet conteneur de classe de schéma, afin que les données de schéma puissent être récupérées au moment de l’exécution.

Les ADsPaths pour les objets de conteneur de classe de schéma définis pour le composant de fournisseur d’exemple sont « Sample://Seattle/schema » et « Sample://Toronto/schema ». Dans cet exemple, le contenu des schémas est identique.

 

 