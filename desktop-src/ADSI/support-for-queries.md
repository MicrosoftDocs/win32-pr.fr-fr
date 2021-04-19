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
# <a name="support-for-queries"></a><span data-ttu-id="da4bf-104">Prise en charge des requêtes</span><span class="sxs-lookup"><span data-stu-id="da4bf-104">Support for Queries</span></span>

<span data-ttu-id="da4bf-105">En implémentant l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , les fournisseurs ADSI obtiennent un accès à un sous-ensemble de OLE DB fonctionnalités en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="da4bf-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="da4bf-106">L’implémentation ADSI des méthodes de [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) elle-même utilise les interfaces de OLE DB décrites dans ADSI version 1,0, y compris la liste suivante d’objets com :</span><span class="sxs-lookup"><span data-stu-id="da4bf-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="da4bf-107">Objet de source de données (service d’annuaire), prenant en charge **IDBInitialize**, **méthode IDBCreateSession**, **IDBProperties** et **IPersist**.</span><span class="sxs-lookup"><span data-stu-id="da4bf-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="da4bf-108">Objet DBSessions, prenant en charge **IOpenRowSet**, **ISessionProperties** et **ICreateCommand**.</span><span class="sxs-lookup"><span data-stu-id="da4bf-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="da4bf-109">Objet Command, qui prend en charge **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** et **IConvertType**.</span><span class="sxs-lookup"><span data-stu-id="da4bf-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="da4bf-110">Objet Rowset, prenant en charge **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** et **IRowsetInfo**.</span><span class="sxs-lookup"><span data-stu-id="da4bf-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="da4bf-111">Pour plus d’informations sur OLE DB, consultez le Guide de référence du programmeur OLE DB dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="da4bf-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




