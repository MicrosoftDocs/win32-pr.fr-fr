---
title: Liaison de données via IPropertyNotifySink
description: Liaison de données via IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d39c7277d27f0df6c185fc35a926aa98b77b91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675709"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Liaison de données via IPropertyNotifySink

Les objets qui prennent en charge des propriétés, par exemple, par le biais d’OLE Automation et de l’interface **IDispatch** , peuvent souhaiter autoriser les clients à être avertis lorsque certaines propriétés changent de valeur. Une telle propriété est appelée une propriété pouvant être liée, car les notifications permettent à un client de synchroniser son propre affichage des valeurs de propriété actuelles de l’objet. En outre, les mêmes objets peuvent permettre à un client de contrôler le moment auquel certaines propriétés peuvent être modifiées. Ces propriétés sont appelées propriétés de modification de demande.

[**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) est une interface de notification standard qui prend en charge les propriétés bindables et de modification de requête. **IPropertyNotifySink** est pris en charge à partir d’un objet avec des propriétés en tant qu’interface sortante. Autrement dit, l’interface elle-même est implémentée par l’objet récepteur d’un client, et le client connecte le récepteur à l’objet de prise en charge via le mécanisme de point de connexion décrit précédemment. **IPropertyNotifySink** est défini comme suit :

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Lorsqu’un objet souhaite notifier ses récepteurs connectés qu’une propriété pouvant être liée identifiée par un DISPID donné a changé, il appelle [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Si un objet modifie plusieurs propriétés à la fois, il peut passer DISPID \_ inconnu à **OnChanged** , auquel cas un client actualise son cache de toutes les valeurs de propriété intéressantes.

Quand une propriété de modification de requête est sur le paragraphe de changer, un objet peut demander au client s’il autorise la modification. L’objet appelle [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) en passant le DISPID de la propriété en question (ou DISPID \_ inconnu pour identifier toutes les propriétés). Le récepteur du client retourne la valeur \_ OK pour indiquer que la modification est autorisée ou \_ false (ou une erreur) pour indiquer que la modification n’est pas autorisée. Quand un objet appelle **OnRequestEdit**, il doit respecter les souhaits du client en suivant la sémantique exacte des valeurs de retour de s \_ OK et s \_ false.

Notez que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) ne peut pas être utilisé pour la validation des données, car au moment de l’appel, la nouvelle valeur de la propriété n’est pas encore disponible. La notification ne peut être utilisée que pour contrôler un État en lecture seule pour une propriété.

Les objets contrôlent les propriétés qui peuvent être liées et demandent la modification et marquent ces propriétés dans les informations de type de l’objet. Dans les informations de type, l’attribut pouvant être lié marque une propriété comme prenant en charge [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). L’attribut modification marque une propriété en tant que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit)de prise en charge.

Une propriété peut prendre en charge les deux comportements, dans lesquels cas [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) est appelé en premier, et uniquement si la modification est autorisée est [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) appelée.

La seule exception au comportement de telles propriétés est qu’aucune notification n’est envoyée à la suite des procédures d’initialisation ou de chargement d’un objet. À ce moment-là, il est supposé que toutes les propriétés changent et que toutes les modifications doivent être autorisées. Les notifications à cette interface sont par conséquent uniquement significatives dans le contexte d’un objet entièrement initialisé/chargé.

Deux autres attributs peuvent être appliqués aux propriétés dans les informations de type d’un objet. L’attribut defaultbind marque une propriété pouvant être liée comme étant celle qui correspond le mieux à l’état de l’objet dans son ensemble. L’attribut DisplayBind marque une propriété pouvant être liée comme pouvant être affichée dans l’interface utilisateur d’un client.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pages de propriétés et feuilles de propriétés](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




