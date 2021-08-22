---
title: Stockage et objets de flux pour un jeu de propriétés
description: Le programmeur spécifie si un jeu de propriétés est stocké dans un stockage ou un flux lorsque le jeu de propriétés est créé.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e63ff148a72342da4cf5a6d8e1d59feab5c9b5b6fcbdf8a413069413cdb1e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661839"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Stockage et objets de flux pour un jeu de propriétés

Le programmeur spécifie si un jeu de propriétés est stocké dans un stockage ou un flux lorsque le jeu de propriétés est créé. La \_ valeur d’énumération PROPSETFLAG insimple, passée dans le paramètre *grfFlags* à la méthode [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , indique cela. La définition de l’emplacement de stockage du jeu de propriétés fournit des contrôles d’application appropriés pour interagir entièrement via l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) avec le jeu de propriétés com.

Si l' \_ indicateur PROPSETFLAG non simple est défini, le jeu de propriétés est stocké dans un objet de stockage et des valeurs de propriété non simples peuvent y être écrites. Les valeurs qui ne sont pas simples incluent des valeurs avec un **VarType** de \_ stockage VT, un flux VT, un \_ \_ objet stocké VT \_ ou un \_ objet transmis en continu VT \_ . Pour plus d’informations sur les valeurs **VarType** et leur utilisation, consultez la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Si l' \_ indicateur PROPSETFLAG non simple n’est pas défini, seules des valeurs simples peuvent être écrites dans le jeu de propriétés.

Dans l’objet de stockage d’un jeu de propriétés non simple, un flux est créé nommé contents. Il s’agit du flux principal du jeu de propriétés qui contient toutes les valeurs de propriété simples. Les valeurs de propriété qui ne sont pas simples (flux et stockages) sont stockées sous l’objet de stockage principal de la propriété définie en tant que sous-flux et stockages. Autrement dit, ces valeurs non simples sont stockées en tant que frères dans le flux de contenu. Le nom des flux et des stockages frères est déterminé par l’implémentation et stocké dans le flux de contenu similaire à la façon dont une propriété de chaîne simple est stockée.

 

 