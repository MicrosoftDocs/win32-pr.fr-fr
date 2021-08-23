---
title: CPROVCF. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code du code de fabrique de classe d’objet du fournisseur ADs se trouve dans cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3b77ea7fe1b1d6fe946b9a8b509be33c11f2a075ee658ee305f0f7ba2d2c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023667"
---
# <a name="cprovcfcpp"></a>CPROVCF. COTISATIONS

Dans l’exemple de composant fournisseur, un exemple de code du code de fabrique de classe d’objet du fournisseur ADs se trouve dans cprovcf. cpp. le composant fournisseur ne crée jamais directement une instance de cet objet à un moment autre que lorsque l’objet est créé automatiquement pendant les opérations de liaison dans [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou dans la fonction interne de la méthode Visual Basic **GetObject**. La méthode prise en charge est présentée dans le tableau suivant.



| Méthode                                  | Description                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF :: CreateInstance** | Crée une instance de la fabrique de classes pour l’objet fournisseur ADS. |



 

 

 




