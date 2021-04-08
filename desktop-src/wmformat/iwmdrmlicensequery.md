---
title: Interface IWMDRMLicenseQuery
description: L’interface IWMDRMLicenseQuery permet aux applications d’interroger les droits et l’état de licence d’un fichier protégé.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Format Windows Media de l’interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728716"
---
# <a name="iwmdrmlicensequery-interface"></a>Interface IWMDRMLicenseQuery

L’interface **IWMDRMLicenseQuery** permet aux applications d’interroger les droits et l’état de licence d’un fichier protégé. Cette interface utilise l’ID de clé pour exécuter des requêtes sur le magasin de licences local.

Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md). Transmettez **IID \_ IWMDRMLicenseQuery** comme paramètre *riid* .

## <a name="members"></a>Membres

L’interface **IWMDRMLicenseQuery** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseQuery** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMLicenseQuery** possède ces méthodes.



| Méthode                                                                                | Description                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)                   | Interroge le magasin de licences local pour obtenir les autorisations nécessaires pour effectuer des actions par ID de clé.<br/>         |
| [**QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md)                     | Interroge le magasin de licences local pour obtenir les données d’état de licence par ID de clé et les droits spécifiques.<br/> |
| [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) | Définit des paramètres environnementaux pour améliorer la précision des requêtes de licence.<br/>             |



 

## <a name="remarks"></a>Notes

Les méthodes de **IWMDRMLicenseQuery** ne fournissent pas d’informations sur les licences individuelles. Au lieu de cela, les données de licence sont agrégées par le sous-système DRM avant le renvoi des résultats de la requête.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

