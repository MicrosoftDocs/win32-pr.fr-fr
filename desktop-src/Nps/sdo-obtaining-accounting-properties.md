---
title: Obtention des propriétés de gestion des comptes
description: L’objet Accounting est l’un des objets de la collection de gestionnaires de demandes.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77390a6aa67e946de6d69dd3d1bc28a76907b7ad31b497d4921c7a2d7493c328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361727"
---
# <a name="obtaining-accounting-properties"></a>Obtention des propriétés de gestion des comptes

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

L’objet Accounting est l’un des objets de la collection de gestionnaires de demandes. La valeur d’énumération pour la collection de gestionnaires de demandes est la propriété de la **\_ \_ \_ collection REQUESTHANDLERS IAS**. Le nom du gestionnaire de l’objet de gestion des comptes est « Microsoft Accounting ».

le code Visual Basic suivant accède aux propriétés disponibles à partir du gestionnaire d’objets de comptabilité.


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



Pour accéder aux propriétés de gestion de comptes à l’aide de C++, obtenez d’abord la collection de gestionnaires de demandes. La [récupération d’une collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contient du code C++ qui montre comment obtenir une collection. La valeur d’énumération pour la collection de gestionnaires de demandes est la propriété de la **\_ \_ \_ collection REQUESTHANDLERS IAS**. (Les valeurs correspondant aux différentes collections NPS sont énumérées par le type d’énumération [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .)

La collection de gestionnaires de demandes contient un objet nommé « Microsoft Accounting ». Récupérez cet objet de la collection. La section [récupération d’un objet d’une collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contient du code C++ qui montre comment obtenir un objet à partir d’une collection.

Une fois que vous disposez de l’objet Microsoft Accounting, obtenez une interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) pour l’objet à l’aide de [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). La section [récupération d’un utilisateur SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contient du code C++ qui montre comment obtenir une interface **ISdo** pour un objet. Vous pouvez ensuite utiliser la méthode [**ISdo :: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) pour obtenir les valeurs de propriété de l’objet Microsoft Accounting.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Récupération d’une collection](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Récupération d’un objet à partir d’une collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Récupération d’un utilisateur SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 