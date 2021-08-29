---
title: Objets et propriétés
description: Les caractéristiques d’un objet dans SDO sont déterminées par les propriétés de l’objet et les valeurs associées à ces propriétés.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbf871f6aa1e36c3d93eb93853660d0aa9b083d89f4030446fedd8c883530694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128619"
---
# <a name="objects-and-properties"></a>Objets et propriétés

Les caractéristiques d’un objet dans SDO sont déterminées par les propriétés de l’objet et les valeurs associées à ces propriétés. Contrairement à d’autres modèles objet, les objets SDO eux-mêmes n’ont pas de méthodes. Toutefois, les objets SDO exposent des interfaces COM qui fournissent des méthodes.

Les objets dans SDO exposent l’interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) qui fournit des méthodes pour manipuler les propriétés des objets. Pour accéder aux propriétés de l’objet, obtenez une interface **ISdo** pour l’objet et utilisez les méthodes de l’interface [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) et [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) pour récupérer et définir les valeurs des propriétés. La rubrique [récupération d’un utilisateur SDO contient un](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) exemple de code qui illustre l’obtention de l’interface **ISdo** pour un objet utilisateur.

Après avoir apporté des modifications aux propriétés d’un objet, utilisez la méthode [**ISdo :: apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) pour écrire les modifications dans le stockage persistant de l’objet. Vous pouvez annuler les modifications apportées aux propriétés d’un objet avant d’appeler **ISdo :: apply** en appelant la méthode [**ISdo :: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) . Cette méthode restaure les valeurs des propriétés d’un objet à partir d’un stockage persistant.

Le tableau suivant présente les types d’énumération qui énumèrent les propriétés de certains objets dans SDO.



| Object                                 | Type d'énumération                                       |
|----------------------------------------|--------------------------------------------------------|
| Tous les objets SDO                        | [**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| Objet utilisateur                            | [**USERPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Objet de service (serveur de stratégie réseau) | [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Objet de protocole RADIUS Microsoft       | [**RADIUSPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008.

 

## <a name="collections"></a>Collections

Les objets sont souvent regroupés dans des collections. L’API SDO fournit des fonctionnalités, via l’interface de [**collection ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , pour énumérer les objets dans une collection et pour ajouter et supprimer des objets d’une collection.

L’accès à une collection est obtenu en extrayant une propriété de collection sur l’objet qui contient la collection. Pour plus d’informations, consultez la section [hiérarchie du modèle objet](/windows/desktop/Nps/sdo-object-model-hierarchy).

Le type de données pour toutes les propriétés qui correspondent aux collections est VT \_ Dispatch.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hiérarchie du modèle objet SDO](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Attributs pris en charge par SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 