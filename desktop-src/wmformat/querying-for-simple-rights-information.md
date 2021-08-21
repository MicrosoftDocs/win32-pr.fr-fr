---
title: Interrogation des informations de droits simples
description: Interrogation des informations de droits simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media Format SDK, interrogation de droits simples
- Windows Media Format SDK, requêtes de droits simples
- gestion des droits numériques (DRM), interrogation de droits simples
- DRM (Digital Rights Management), interrogation de droits simples
- gestion des droits numériques (DRM), requêtes de droits simples
- DRM (gestion des droits numériques), requêtes de droits simples
- API étendues du client DRM, interrogation de droits simples
- API étendues clientes, interrogation de droits simples
- API étendues du client DRM, requêtes de droits simples
- API étendues clientes, requêtes de droits simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0686616bbc700c51a005c3e1e63eed889c42965aaebbba232fcf90b9cce26987
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027367"
---
# <a name="querying-for-simple-rights-information"></a>Interrogation des informations de droits simples

les api étendues du Client Windows Media DRM vous permettent d’obtenir rapidement des informations simples sur le fait d’accéder à du contenu protégé pour différentes actions.

La méthode [**IWMDRMLicenseQuery :: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) peut être utilisée pour déterminer rapidement si une action est autorisée par une licence dans le magasin de licences local. **QueryActionAllowed** a été optimisé pour être beaucoup plus rapide que les requêtes pour obtenir des informations similaires à l’aide des objets du kit de développement logiciel (SDK) Windows Media Format. Toutefois, ce type de requête agrège les licences dans le magasin de licences local et ne doit être utilisé que pour des fonctionnalités simples, telles que peut être nécessaire pour les éléments de l’interface utilisateur, par exemple l’affichage d’un indicateur d’autorisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Obtention d’informations à partir de licences dans le magasin de licences local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




