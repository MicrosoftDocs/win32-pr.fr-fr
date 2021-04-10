---
title: Définition de l’identificateur de classe du jeu de propriétés
description: La méthode IPropertyStorage SetClass définit à la fois le CLSID de l’objet de stockage et la valeur de balise de classe stockée dans le jeu de propriétés COM. Cela se produit lorsqu’il est appelé sur un stockage de propriété non simple stocké dans un objet de stockage structuré.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Définition de l’identificateur de classe du jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029651"
---
# <a name="setting-the-property-set-class-identifier"></a>Définition de l’identificateur de classe du jeu de propriétés

La méthode [**IPropertyStorage :: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) définit à la fois le CLSID de l’objet de stockage et la valeur de balise de classe stockée dans le jeu de propriétés com. Cela se produit lorsqu’il est appelé sur un stockage de propriété non simple stocké dans un objet de stockage structuré.

Cela fournit une cohérence et une uniformité qui crée une meilleure interaction avec certains outils. Un objet de stockage de propriétés n’est pas simple s’il est créé en appelant [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) avec l’indicateur **PROPSETFLAG non \_ simple** défini.

Le CLSID de l’objet de stockage est défini avec un appel à [**IStorage :: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).

 

 




