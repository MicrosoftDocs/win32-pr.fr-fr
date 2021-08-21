---
title: Persistance
description: Persistance
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c8600307bfe6c29f72fb9d29e633358062c4e8c1c61da8898173cf190f1d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500329"
---
# <a name="persistence"></a>Persistance

Un contrôle implémente une ou plusieurs des différentes interfaces de persistance pour prendre en charge la persistance de son état. Par exemple, l’interface [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) prend en charge la persistance basée sur le flux de l’état du contrôle. **IPersistStreamInit** remplace [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) et ajoute une méthode d’initialisation, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew). Les autres méthodes sont les mêmes dans les deux interfaces. **IPersistStreamInit** n’est pas dérivé de **IPersistStream**; un objet ne prend en charge qu’une seule des deux interfaces selon qu’il a besoin de pouvoir initialiser de nouvelles instances de lui-même.

Les autres interfaces de persistance qu’un contrôle peut offrir incluent : [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). L’implémenteur de contrôle doit décider quels types de persistance sont les plus importants et implémenter les interfaces de persistance appropriées. L’implémenteur de contrôle décide également ce qui doit être enregistré. Par exemple, un contrôle peut enregistrer les valeurs actuelles de ses propriétés ou son emplacement et sa taille dans son conteneur. Le client décide de l’interface qu’il préfère utiliser.

Avant de charger un contrôle à partir de son état persistant, un client peut vérifier l' \_ indicateur OLEMISC SETCLIENTSITEFIRST pour déterminer si le contrôle prend en charge l’obtention de son site client et les propriétés ambiantes avant de charger son état persistant. Cette optimisation peut gagner du temps lors de l’instanciation d’un contrôle, car le contrôle est ensuite libre d’ignorer ses valeurs persistantes plutôt que de les charger uniquement pour qu’elles soient remplacées par les propriétés ambiantes fournies par le client.

Un contrôle peut également prendre en charge l’enregistrement et la restauration de son état dans un jeu de propriétés OLE, un ensemble d’identificateurs et de valeurs dans un format spécifié. cette fonctionnalité peut être utile avec les conteneurs tels que Visual Basic, qui enregistre ses programmes sous une forme textuelle. Un contrôle qui souhaite prendre en charge cette fonctionnalité implémente [**IDataObject :: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) et [**IDataObject :: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) pour passer ses valeurs de propriété vers et à partir du conteneur, respectivement. Il s’agit de la tâche du conteneur pour convertir ces informations en texte et les enregistrer. Les identificateurs utilisés par le contrôle correspondent aux noms de propriété du contrôle et aux valeurs. Consultez le CDK OLE pour la définition de ce jeu de propriétés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Commandes](activex-controls.md)
</dt> </dl>

 

 