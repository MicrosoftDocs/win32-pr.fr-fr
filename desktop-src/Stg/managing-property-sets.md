---
title: Gestion des jeux de propriétés
description: Un jeu de propriétés persistantes contient des données associées sous forme de propriétés.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Gestion des jeux de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3f9862d3074a5221bf1d5d975754486a562f87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008913"
---
# <a name="managing-property-sets"></a>Gestion des jeux de propriétés

Un jeu de propriétés persistantes contient des données associées sous forme de propriétés. Chaque jeu de propriétés est identifié par un FMTID et un identificateur global unique (GUID) qui permet aux applications d’accéder au jeu de propriétés, afin d’identifier le jeu de propriétés. Par le biais de cette identification, l’application interprète les propriétés contenues dans le jeu.

Par exemple, les propriétés de mise en forme des caractères dans un traitement de texte ou les attributs de rendu d’un élément dans un programme de dessin sont des jeux de propriétés.

COM définit l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour faciliter la gestion des jeux de propriétés. À l’aide des méthodes de cette interface, vous pouvez créer un nouveau jeu de propriétés ou ouvrir ou supprimer un jeu de propriétés existant. En outre, il fournit une méthode qui crée un énumérateur et fournit un pointeur vers son interface [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Vous pouvez appeler les méthodes de cette interface pour énumérer les structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sur votre objet, ce qui fournit des informations sur tous les jeux de propriétés de l’objet.

Lorsque vous créez ou ouvrez une instance de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), elle est semblable à l’ouverture d’un objet qui prend en charge [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), car vous devez spécifier le mode de stockage dans lequel vous ouvrez l’interface. Pour **IStorage**, ceux-ci incluent le mode de transaction, le mode lecture/écriture et le mode de partage.

Lorsque vous créez un jeu de propriétés à l’aide d’un appel à [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), spécifiez si le jeu de propriétés doit être simple ou non simple. un jeu de propriétés simple contient des types qui peuvent être écrits entièrement dans le flux de jeu de propriétés, dont la taille est limitée, et ne peut pas dépasser 256 ko dans Windows NT 4,0 et versions antérieures, ou 1 mo dans Windows 2000, Windows XP et Windows Server 2003. Toutefois, lorsque vous avez besoin de stocker une plus grande quantité d’informations dans le jeu de propriétés, vous pouvez spécifier que le jeu de propriétés n’est pas simple. Cela vous permet d’utiliser un ou plusieurs des types qui spécifient uniquement un pointeur vers un objet de stockage ou de flux. Ces types sont VT \_ Stream, VT \_ streaming Object, VT \_ Storage et VT \_ Stored \_ Object.

les données stockées dans ces propriétés ne sont pas comptabilisées par rapport à la limite de taille définie pour la propriété 256 KB dans Windows NT 4,0 ou version antérieure, ou la limite de 1 mo dans Windows 2000, Windows XP et Windows Server 2003. Toutefois, les données relatives à la propriété, telles que son nom, s’appliquent. En outre, si vous avez besoin d’une mise à jour avec transaction, le jeu de propriétés doit être insimple. Il existe, bien sûr, une certaine baisse des performances pour l’ouverture de ces types, car cela nécessite l’ouverture du flux ou de l’objet de stockage auquel vous avez le pointeur.

Si votre application utilise des fichiers composés, vous pouvez utiliser l’implémentation fournie par COM de ces interfaces, qui sont implémentées sur l’objet de stockage de fichiers composés COM.

Chaque jeu de propriétés se compose principalement d’un groupe de propriétés connecté de manière logique, comme décrit dans [gestion des propriétés](managing-properties.md).

Pour plus d’informations sur les jeux de propriétés dans COM, consultez :

-   [Implémentations de jeux de propriétés dans COM](property-set-implementations-in-com.md)
-   [Considérations relatives aux jeux de propriétés](property-set-considerations.md)
-   [Considérations relatives à l’implémentation de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Stockage des jeux de propriétés](storing-property-sets.md)
-   [Caractéristiques de performances](performance-characteristics.md)
-   [Implémentation du jeu de propriétés d’informations de résumé](implementing-the-summary-information-property-set.md)

 

 