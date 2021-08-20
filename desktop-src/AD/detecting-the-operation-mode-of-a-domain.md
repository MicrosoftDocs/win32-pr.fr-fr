---
title: Détection du mode d’opération d’un domaine
description: dans Windows 2000, un domaine peut s’exécuter en deux modes d’opération mixtes et natifs.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Détection du mode d’opération d’un domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cd704c36835997f509e041e12b820b223571dd27dffc6a5920b8ff623d93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019360"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a>Détection du mode d’opération d’un domaine

dans Windows 2000, un domaine peut s’exécuter dans deux modes d’opération : mixte et natif. le mode mixte doit être utilisé pour inclure les contrôleurs de domaine exécutant Windows NT 4,0 dans un domaine Windows 2000. Le mode mixte ne prend pas en charge les groupes universels ni les groupes imbriqués. si tous les contrôleurs de domaine du domaine exécutent Windows 2000, vous pouvez utiliser le mode natif.

pour détecter par programme le mode d’opération d’un domaine Windows 2000, lisez la propriété [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) de l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) pour ce domaine. La valeur zéro (0) signifie que le domaine est en mode natif. La valeur un (1) indique que le domaine est en mode mixte. Vous pouvez également utiliser la fonction [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) pour obtenir le mode d’opération ainsi que d’autres données sur le domaine et son état.

Pour établir une liaison avec l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) du domaine du compte d’utilisateur sous lequel votre application s’exécute, utilisez une liaison sans serveur et RootDSE pour obtenir le nom unique du domaine, puis utilisez ce nom unique pour établir une liaison à l’objet **domainDNS** qui représente ce domaine. Pour plus d’informations sur la liaison sans serveur et rootDSE, consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).

Pour plus d’informations et pour obtenir un exemple de code qui montre comment détecter par programme le mode d’opération d’un domaine, consultez l' [exemple de code permettant de déterminer le mode d’opération](example-code-for-determining-the-operation-mode.md).

 

 