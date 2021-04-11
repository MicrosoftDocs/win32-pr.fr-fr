---
title: Création de licences localement
description: Création de licences localement
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows Media Format SDK, création de licences localement
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), création de licences localement
- DRM (gestion des droits numériques), création de licences localement
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, création de licences locales
- API étendues clientes, création de licences localement
- licences, créer des licences localement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029829"
---
# <a name="creating-licenses-locally"></a>Création de licences localement

Dans certaines circonstances, par exemple lors de l' [importation de DRM](drm-import.md), vous pouvez créer vos propres licences. Les licences Windows Media DRM peuvent être écrites de différentes manières, mais pour créer votre propre licence, vous devez utiliser le schéma binaire XMR (extensible Media Rights). Pour plus d’informations, consultez [génération d’une licence XMR](building-an-xmr-license.md).

Lorsque vous créez une licence, vous pouvez l’ajouter au magasin de licences local en appelant la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Acquisition de licences**](acquiring-licenses.md)
</dt> <dt>

[**Génération d’une licence XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




