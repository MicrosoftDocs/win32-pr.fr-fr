---
title: Prise en charge des requêtes
description: En implémentant l’interface IDirectorySearch, les fournisseurs ADSI obtiennent un accès à un sous-ensemble de OLE DB fonctionnalités en lecture seule.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Prise en charge des requêtes ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517936"
---
# <a name="support-for-queries"></a>Prise en charge des requêtes

En implémentant l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , les fournisseurs ADSI obtiennent un accès à un sous-ensemble de OLE DB fonctionnalités en lecture seule.

L’implémentation ADSI des méthodes de [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) elle-même utilise les interfaces de OLE DB décrites dans ADSI version 1,0, y compris la liste suivante d’objets com :

-   Objet de source de données (service d’annuaire), prenant en charge **IDBInitialize**, **méthode IDBCreateSession**, **IDBProperties** et **IPersist**.
-   Objet DBSessions, prenant en charge **IOpenRowSet**, **ISessionProperties** et **ICreateCommand**.
-   Objet Command, qui prend en charge **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** et **IConvertType**.
-   Objet Rowset, prenant en charge **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** et **IRowsetInfo**.

Pour plus d’informations sur OLE DB, consultez le Guide de référence du programmeur OLE DB dans le kit de développement logiciel (SDK) de la plateforme.

 

 




