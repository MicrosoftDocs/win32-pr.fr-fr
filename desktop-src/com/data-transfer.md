---
title: Transfert de données
description: Transfert de données
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98e7f546cab245e1f2d2d06036379ea5b28526edcf42aa8a364ea04688db034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993486"
---
# <a name="data-transfer"></a>Transfert de données

Le modèle COM (Component Object Model) fournit un mécanisme standard pour transférer des données entre les applications. Ce mécanisme est l' *objet de données*, qui est tout simplement un objet com qui implémente l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Certains objets de données, tels qu’un morceau de texte copié dans le presse-papiers, possèdent **IDataObject** comme seule interface. D’autres, telles que les objets de document composé, exposent plusieurs interfaces dont **IDataObject** est tout simplement un. Les objets de données sont fondamentaux pour le travail des documents composés, bien qu’ils aient également une application généralisée en dehors de cette technologie OLE.

En échangeant des pointeurs vers un objet de données, les fournisseurs et les consommateurs de données peuvent gérer les transferts de données de manière uniforme, quel que soit le format des données, le type de support utilisé pour transférer les données ou l’appareil cible sur lequel ils doivent être rendus. Vous pouvez inclure la prise en charge dans votre application pour les transferts de base du presse-papiers, les transferts par glisser-déplacer et les transferts de documents composés OLE avec une seule implémentation de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). Cela fait, la quantité de code nécessaire pour prendre en charge la sémantique spéciale de chaque protocole est minime.

Pour plus d'informations, voir les rubriques suivantes :

-   [Interfaces Transfert de données](data-transfer-interfaces.md)
-   [Formats de données et média de transfert](data-formats-and-transfer-media.md)
-   [Glisser-déposer](drag-and-drop.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

 




