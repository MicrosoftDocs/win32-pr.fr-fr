---
description: Navigation dans la hiérarchie de regroupement COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navigation dans la hiérarchie de regroupement COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538630"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navigation dans la hiérarchie de regroupement COM+

Quelques collections que vous pouvez récupérer facilement à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur l’objet [**COMAdminCatalog**](comadmincatalog.md) . Cette méthode récupère une collection « de niveau supérieur »; autrement dit, une collection telle que [**applications**](applications.md), qui est autonome et qui est unique et ne peut pas être incluse logiquement sous une autre collection.

De nombreux regroupements, toutefois, sont logiquement inclus dans une autre collection, car ils contiennent des éléments qui font partie d’une structure plus grande. Par exemple, la collection de [**composants**](components.md) est incluse, ou associée, à la collection d' [**applications**](applications.md) , car elle contient les composants installés dans une application com+ particulière, qui correspond elle-même à un élément dans la collection d' **applications** . Les regroupements associés tels que celui-ci ne sont pas uniques. Il existe une collection de **composants** pour chaque application distincte.

Par conséquent, les collections sont organisées dans une structure hiérarchique qui correspond naturellement aux relations logiques entre les éléments qu’elles contiennent. Vous trouverez un diagramme de la hiérarchie de collection dans les [collections d’administration com+](com--administration-collections.md). Pour la plupart des éléments que vous souhaitez configurer à l’aide des objets comadmin, vous devez parcourir certaines parties de la hiérarchie de collection pour récupérer l’élément approprié.

Dans la pratique, cela signifie que si vous souhaitez obtenir un élément dans un regroupement connexe, vous devez d’abord parcourir tous les regroupements inclus dont fait nécessaires. Et pour récupérer un regroupement connexe, vous devez récupérer l’élément spécifique dans le regroupement parent auquel la collection enfant est associée. Par exemple, si vous souhaitez configurer un élément correspondant à un composant dans une application COM+ particulière, vous devez effectuer les étapes suivantes :

1.  Récupérez la collection d' [**applications**](applications.md) et remplissez-la.
2.  Énumérez le contenu de la collection d' [**applications**](applications.md) jusqu’à ce que vous obteniez l’élément correspondant à l’application com+ appropriée.
3.  Obtenir et remplir la collection de [**composants**](components.md) pour cette application com+ particulière.
4.  Énumérez le contenu de la collection de [**composants**](components.md) jusqu’à ce que vous obteniez l’élément correspondant au composant approprié.

L’exemple de Visual Basic Microsoft suivant montre comment effectuer les étapes précédentes :


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



Deux méthodes **GetCollection** distinctes sont utilisées dans l’exemple précédent. Le premier est exposé par [**COMAdminCatalog**](comadmincatalog.md) et est utilisé pour obtenir une collection de niveau supérieur, dans le cas présent, « applications ». Le deuxième est exposé par [**COMAdminCatalogCollection**](comadmincatalogcollection.md) et est utilisé pour obtenir une collection liée à la collection actuelle. vous indiquez précisément la collection que vous souhaitez en passant le nom « Components » et la valeur de propriété de clé de l’objet parent. La valeur de la propriété de clé est souvent un nom ou un GUID qui identifie l’objet de façon unique ; Cette valeur est identifiée dans la documentation de chaque collection.

Dans le cas le plus général, vous devez obtenir les collections associées de manière itérative dans la hiérarchie de collection jusqu’à ce que vous récupériez le regroupement de votre choix. Les étapes à suivre pour suivre le même modèle général, de façon répétée. Pour obtenir la liste complète des regroupements, consultez [regroupements d’administration com+](com--administration-collections.md).

Dans certains cas, vous souhaiterez peut-être utiliser une méthode de raccourci la deuxième fois que vous suivez un chemin d’accès dans la hiérarchie de collection. Vous pouvez utiliser cette méthode uniquement après avoir déjà mis en cache toutes les valeurs de clé intermédiaires. Pour plus d’informations, consultez [**ICOMAdminCatalog :: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Remplissage des collections COM+](populating-com--collections.md)
</dt> <dt>

[Interrogation des collections associées disponibles](querying-for-available-related-collections.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



