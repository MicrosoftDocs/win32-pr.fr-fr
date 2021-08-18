---
title: Utilisation de l’interface IDirectoryObject
description: Lorsque vous créez un client ADSI en C ou C++ qui utilise la liaison précoce, vous disposez d’une plus grande variété de types de données ADSI utilisables pour votre client s’il appelle l’interface IDirectoryObject au lieu de l’interface IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, utilisation
- ADSI ADSI, à l’aide de, à l’aide de l’interface IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d085344e5d2d1afe975dd347ff9e9cf4cdad99c1177819e0094b7a83f2219fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023080"
---
# <a name="using-the-idirectoryobject-interface"></a>Utilisation de l’interface IDirectoryObject

Lorsque vous créez un client ADSI en C ou C++ qui utilise la liaison précoce, vous disposez d’une plus grande variété de types de données ADSI utilisables pour votre client s’il appelle l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) au lieu de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . L’interface **IDirectoryObject** fournit des méthodes pour prendre en charge un sous-ensemble des propriétés de maintenance d’un objet et pour accéder à ses attributs. L’illustration suivante montre les relations entre les structures de données.

![structures de données de l’interface idirectoryobject](images/ds2dso.png)

Dans la figure précédente, les [**\_ \_ informations sur l’objet structure ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info) définissent les propriétés qui identifient l’objet par nom unique, nom unique relatif, par conteneur (ParentDN), par type d’objet (ClassDN) et par définition de schéma (SchemaDN). Le descripteur d’attribut [**ADS \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) se compose d’un nom, d’un type de données, d’un tableau de valeurs de données affichées dans [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)et d’un indicateur qui indique au service d’annuaire sous-jacent d’effectuer certaines opérations sur les attributs détaillés dans les [ \_ \_ \* constantes de publicités attr](adsi-constants.md). Les types de données de ces attributs incluent les types syntaxiques étendus ADSI, détaillés dans [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).

 

 




