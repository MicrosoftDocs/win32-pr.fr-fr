---
title: Documents composés
description: Les documents composés OLE permettent aux utilisateurs qui travaillent au sein d’une même application de manipuler des données écrites dans différents formats et dérivées de plusieurs sources.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102448"
---
# <a name="compound-documents"></a>Documents composés

Les documents composés OLE permettent aux utilisateurs qui travaillent au sein d’une même application de manipuler des données écrites dans différents formats et dérivées de plusieurs sources. Par exemple, un utilisateur peut insérer dans un document de traitement de texte un graphique créé dans une deuxième application et un objet son créé dans une troisième application. L’activation du graphique entraîne le chargement de l’interface utilisateur de la deuxième application, ou au moins de la partie contenant les outils nécessaires à la modification de l’objet. L’activation de l’objet Sound entraîne la lecture de la troisième application. Dans les deux cas, un utilisateur est en mesure de manipuler des données à partir de sources externes à partir du contexte d’un document unique.

La technologie OLE Compound document repose sur une Fondation composée de COM, de stockage structuré et de transfert de données uniforme. Comme résumé ci-dessous, chacune de ces technologies de base joue un rôle essentiel dans les documents composés OLE :

<dl> <dt>

<span id="COM"></span><span id="com"></span>COM
</dt> <dd>

Un objet de document composé est essentiellement un objet COM qui peut être incorporé dans un document existant ou lié à celui-ci. En tant qu’objet COM, un objet de document composé expose l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , par l’intermédiaire de laquelle les clients peuvent obtenir des pointeurs vers ses autres interfaces, y compris plusieurs, telles que [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)et [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), qui fournissent des fonctionnalités spéciales propres aux objets de document composés.

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Stockage structuré
</dt> <dd>

Un objet de document composé doit implémenter les interfaces [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) ou, éventuellement, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) pour gérer son propre stockage. Un conteneur utilisé pour créer des documents composés doit fournir l’interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , par l’intermédiaire de laquelle les objets stockent et récupèrent les données. Les conteneurs fournissent presque toujours des instances de **IStorage** obtenues à partir de l’implémentation des fichiers composés d’OLE. Les conteneurs doivent également utiliser les interfaces **IPersistStorage** et/ou **IPersistStream** d’un objet.

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer
</dt> <dd>

Les applications qui prennent en charge les documents composés doivent implémenter [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , car les objets incorporés et les objets liés commencent comme des données qui ont été transférées à l’aide de formats de presse-papiers OLE spéciaux, plutôt que des formats de presse-papiers Microsoft Windows standard En d’autres termes, la mise en forme des données en tant qu’objet incorporé ou lié est simplement une option supplémentaire fournie par le modèle de transfert de données uniforme d’OLE.

</dd> </dl>

La technologie des documents composés d’OLE tire parti des développeurs de logiciels et des utilisateurs. Au lieu de vous sentir obligé de récolter chaque fonctionnalité concevable dans une seule application, les développeurs de logiciels sont désormais gratuits, s’ils le souhaitent, pour développer des applications plus petites et plus ciblées qui reposent sur d’autres applications pour fournir des fonctionnalités supplémentaires. Dans les cas où un développeur de logiciels décide de fournir une application avec des fonctionnalités au-delà de ses fonctionnalités de base, le développeur peut implémenter ces services supplémentaires comme des dll distinctes, qui sont chargées dans la mémoire uniquement lorsque leurs services sont requis. Les utilisateurs bénéficient de logiciels plus petits, plus rapides et plus efficaces qu’ils peuvent mélanger et faire correspondre en fonction des besoins, en manipulant tous les composants requis à partir d’un seul document maître.

Pour plus d'informations, voir les rubriques suivantes :

-   [Conteneurs et serveurs](containers-and-servers.md)
-   [Liaison et incorporation](linking-and-embedding.md)
-   [Gestionnaires d’objets](object-handlers.md)
-   [Serveurs in-process](in-process-servers.md)
-   [Objets liés et monikers](linked-objects-and-monikers.md)
-   [Notifications](notifications.md)
-   [Interfaces de document composé](compound-document-interfaces.md)
-   [États des objets](object-states.md)
-   [Implémentation de l’activation In-Place](implementing-in-place-activation.md)
-   [Création d’objets liés et incorporés à partir de données existantes](creating-linked-and-embedded-objects-from-existing-data.md)
-   [Afficher la mise en cache](view-caching.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de données](data-transfer.md)
</dt> <dt>

[Stockage structuré](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 