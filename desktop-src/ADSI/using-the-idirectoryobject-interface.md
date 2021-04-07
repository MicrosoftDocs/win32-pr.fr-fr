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
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671105"
---
# <a name="using-the-idirectoryobject-interface"></a>Utilisation de l’interface IDirectoryObject

Lorsque vous créez un client ADSI en C ou C++ qui utilise la liaison précoce, vous disposez d’une plus grande variété de types de données ADSI utilisables pour votre client s’il appelle l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) au lieu de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . L’interface **IDirectoryObject** fournit des méthodes pour prendre en charge un sous-ensemble des propriétés de maintenance d’un objet et pour accéder à ses attributs. L’illustration suivante montre les relations entre les structures de données.

![structures de données de l’interface idirectoryobject](images/ds2dso.png)

Dans la figure précédente, les [**\_ \_ informations sur l’objet structure ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info) définissent les propriétés qui identifient l’objet par nom unique, nom unique relatif, par conteneur (ParentDN), par type d’objet (ClassDN) et par définition de schéma (SchemaDN). Le descripteur d’attribut [**ADS \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) se compose d’un nom, d’un type de données, d’un tableau de valeurs de données affichées dans [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)et d’un indicateur qui indique au service d’annuaire sous-jacent d’effectuer certaines opérations sur les attributs détaillés dans les [ \_ \_ \* constantes de publicités attr](adsi-constants.md). Les types de données de ces attributs incluent les types syntaxiques étendus ADSI, détaillés dans [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).

 

 




