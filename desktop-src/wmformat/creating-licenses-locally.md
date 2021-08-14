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
ms.openlocfilehash: fda1a889e83f093cbd60043b299b7174a6c963663962a66454c5707060e76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433905"
---
# <a name="creating-licenses-locally"></a>Création de licences localement

Dans certaines circonstances, par exemple lors de l' [importation de DRM](drm-import.md), vous pouvez créer vos propres licences. Windows Les licences DRM multimédias peuvent être écrites de différentes manières, mais pour créer votre propre licence, vous devez utiliser le schéma binaire XMR (extensible Media Rights). Pour plus d’informations, consultez [génération d’une licence XMR](building-an-xmr-license.md).

Lorsque vous créez une licence, vous pouvez l’ajouter au magasin de licences local en appelant la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Acquisition de licences**](acquiring-licenses.md)
</dt> <dt>

[**Génération d’une licence XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




