---
title: Fournir des informations sur la classe
description: Fournir des informations sur la classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a042283ca9ba6eb29bceeacef2c32f9bd401ef09e92eafbc737711d0d930336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500119"
---
# <a name="providing-class-information"></a>Fournir des informations sur la classe

Il est souvent utile pour un client d’un objet d’examiner les informations de type de l’objet. À partir du CLSID de l’objet, un client peut localiser la bibliothèque de types de l’objet à l’aide des entrées de Registre, puis peut analyser la bibliothèque de types pour l’entrée de coclasse de la bibliothèque correspondant au CLSID.

Toutefois, tous les objets n’ont pas de CLSID, bien qu’ils aient encore besoin de fournir des informations de type. En outre, il est commode pour un client d’avoir un moyen de demander simplement à un objet ses informations de type au lieu de passer par tous les caractère fastidieux pour extraire les mêmes informations à partir des entrées de registre. Cette fonctionnalité est importante lorsque vous traitez des interfaces sortantes sur des objets connectables. (Pour plus d’informations sur la façon dont les objets connectables offrent cette fonctionnalité, consultez [utilisation de IProvideClassInfo](using-iprovideclassinfo.md) .)

Dans ce cas, un client peut interroger l’objet pour [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Si ces interfaces existent, le client appelle la méthode [**GetClassinfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) pour obtenir les informations de type de l’interface.

En implémentant [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), un objet spécifie qu’il peut fournir des informations de type pour toute la classe. autrement dit, ce qu’il décrirait dans sa section coclasse de sa bibliothèque de types, le cas échéant. [**GetClassinfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) retourne un pointeur **ITypeInfo** qui correspond aux informations de coclasse de l’objet. Grâce à ce pointeur **ITypeInfo** , le client peut examiner toutes les définitions d’interface entrantes et sortantes de l’objet.

L’objet peut également fournir des [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). L’interface **IProvideClassInfo2** est une extension simple de [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) qui permet de récupérer rapidement et facilement les identificateurs d’interface sortants d’un objet pour son jeu d’événements par défaut. **IProvideClassInfo2** est dérivée de **IProvideClassInfo**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> </dl>

 

 




