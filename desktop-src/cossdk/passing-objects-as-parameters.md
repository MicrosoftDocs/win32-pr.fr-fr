---
description: Passage d’objets en tant que paramètres
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Passage d’objets en tant que paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47669d3e3e5af572b6dfd50dcbbefacf5c008971f276408fa87b37ccbed9a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070379"
---
# <a name="passing-objects-as-parameters"></a>Passage d’objets en tant que paramètres

Le service composants en file d’attente COM+ n’active pas la mise en file d’attente pour chaque composant COM existant. Il existe des restrictions sur les types de méthodes qui peuvent être mis en file d’attente. En raison des contraintes de messagerie, les méthodes doivent respecter les règles suivantes :

-   Ils ne doivent contenir que des paramètres d’entrée.
-   Ils ne doivent retourner aucun résultat propre à l’application.

En outre, il existe des restrictions sur les types de paramètres d’entrée qui peuvent être passés à un composant mis en file d’attente. Au moment de l’exécution, le service des composants en file d’attente empaquette les arguments au niveau du client et les transmet au composant serveur à l’aide de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). Des types simples, tels que des entiers et des valeurs booléennes, peuvent être marshalés facilement ; les types plus complexes ne peuvent pas être marshalés sans l’aide.

Dans le cas de la transmission d’un objet via l’appel de méthode d’un composant mis en file d’attente en tant que paramètre, le client passe l’objet à l’enregistreur. L’enregistreur marshale l’objet dans un message Message Queuing et le passe à l’écouteur. Une fois que l’écouteur a sélectionné le message et l’a transmis au lecteur, le lecteur doit réinstancier l’objet pour le distribuer à l’appel de méthode spécifié par le client. En fonction des durées de vie du client et du serveur dans un environnement mis en file d’attente, l’implication est que ces objets doivent être en mesure de marshaler par valeur. Étant donné que COM+ ne fournit pas de sémantique de passage par valeur pour les objets COM standard, l’enregistreur et le lecteur ont besoin d’aide du composant pour marshaler et démarshaler l’objet.

Les références d’objets qui prennent en charge [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) peuvent être utilisées comme paramètres pour les appels de méthode sur les composants en file d’attente. L’objet ne peut pas faire d’hypothèses sur le moment où il sera réinstancié. Par exemple, le serveur peut ne pas être disponible ou le composant serveur ne peut pas être démarré tant que plus tard dans la journée. Les objets qui ne prennent pas en charge **IPersistStream** renverront une erreur.

## <a name="visual-basic-persistable-objects"></a>Visual Basic Objets persistants

Microsoft Visual Basic 6 autorise la création d’objets persistants. Ces objets prennent en charge [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) et peuvent être passés en tant que paramètres aux appels de méthode de composant mis en file d’attente. avant qu’un objet Visual Basic puisse être passé à un composant mis en file d’attente, l’objet persistable doit être initialisé. Pour ce faire, vous pouvez procéder de l’une des deux manières suivantes :

-   si l’application qui crée l’objet persistant est écrite en Visual Basic, le runtime Visual Basic gère automatiquement l’initialisation de l’objet.
-   si l’application qui crée l’objet Visual Basic persistant est écrite dans un langage autre que Visual Basic, tel que Microsoft Visual C++, l’application doit initialiser explicitement le composant en interrogeant l’interface [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) de l’objet persistant ou en appelant la méthode [**IPersistStreamInit :: InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)ou [**IPersistStream :: Load**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load) .

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Jeux d’enregistrements ADO et ensembles de lignes OLE DB

Le passage d' **objets d’ensemble de lignes ADO ou** OLE DB entre les composants permet à un composant de traiter les résultats des requêtes exécutées par un autre composant. Cela est utile lors du déploiement d’une application sur plusieurs ordinateurs. Les objets **Recordset** et rowset peuvent être passés en tant que paramètres de méthode aux composants mis en file d’attente, avec les restrictions suivantes :

-   Les objets **Recordset** côté serveur ne peuvent pas être marshalés à l’aide de [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Seuls les objets **Recordset** côté client peuvent être passés en tant que paramètres à un appel de méthode de composant mis en file d’attente.
-   Si vous travaillez directement avec OLE DB, l’ensemble de lignes OLE DB doit être défini en tant qu’ensemble de lignes côté client.

 

 
