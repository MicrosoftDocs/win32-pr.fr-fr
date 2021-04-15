---
title: CPROVCF. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code du code de fabrique de classe d’objet du fournisseur ADs se trouve dans cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461994"
---
# <a name="cprovcfcpp"></a>CPROVCF. COTISATIONS

Dans l’exemple de composant fournisseur, un exemple de code du code de fabrique de classe d’objet du fournisseur ADs se trouve dans cprovcf. cpp. Le composant fournisseur ne crée jamais directement une instance de cet objet à un moment autre que lorsque l’objet est créé automatiquement pendant les opérations de liaison dans [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou dans la fonction interne de la méthode Visual Basic **GetObject**. La méthode prise en charge est présentée dans le tableau suivant.



| Méthode                                  | Description                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF :: CreateInstance** | Crée une instance de la fabrique de classes pour l’objet fournisseur ADS. |



 

 

 




