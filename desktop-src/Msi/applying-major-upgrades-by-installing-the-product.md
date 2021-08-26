---
description: Une mise à niveau majeure peut être appliquée en installant le nouveau package d’installation pour le produit mis à niveau.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Application de mises à niveau majeures en installant le produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79570051ddbff27b12a11e04e41c37f4babad96ff045bc408e00c2b7164b263a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045679"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Application de mises à niveau majeures en installant le produit

Une mise à niveau majeure peut être appliquée en installant le nouveau package d’installation pour le produit mis à niveau. Les mises à niveau majeures obtenant un code de produit différent de celui du produit d’origine, l’installation de la mise à niveau doit être traitée comme une installation d’un nouveau produit. La mise à niveau peut simplement être installée comme un autre produit. Vous pouvez faire en sorte que le nouveau package d’installation traite la suppression de l’ancien produit en incluant la [table de mise à niveau](upgrade-table.md) et l’action [FindRelatedProducts](findrelatedproducts-action.md) et l' [action RemoveExistingProducts](removeexistingproducts-action.md).

**Pour propager une mise à niveau majeure aux utilisateurs actuels à partir de la ligne de commande**

-   À partir de la ligne de commande, utilisez : **msiexec \[ /i** _chemin d’accès au fichier msi mis à jour_*_\]_*

**Pour propager une mise à niveau majeure à des utilisateurs actuels à partir d’un programme**

-   À partir d’un programme, appelez [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) et spécifiez le chemin d’accès au fichier msi mis à jour.

 

 



