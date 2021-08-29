---
description: vous pouvez installer des produits entiers avec des fonctions de Windows Installer. Les étapes suivantes décrivent l’installation d’un produit.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installation d’une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aad6e130d78bd30b940232aeb6fe1da6508be754fe50b9abb9dbcaa0186562
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327959"
---
# <a name="installing-an-application"></a>Installation d’une application

vous pouvez installer des produits entiers avec des fonctions de Windows Installer. Les étapes suivantes décrivent l’installation d’un produit.

**Pour installer un produit**

1.  Exécutez un produit par le biais de sa séquence d’installation ou de désinstallation en appelant la fonction [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .
2.  Spécifiez le niveau d’installation en appelant la fonction [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .

    Vous pouvez utiliser les paramètres de la fonction [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) pour définir l’état d’installation. Par exemple, vous pouvez définir l’État sur installer localement ou pour installer à partir de la source. Vous pouvez définir la plage de fonctionnalités du produit à inclure en définissant le niveau.

Pour plus d’informations sur l’installation d’une application, consultez [résilience](resiliency.md) et [mécanisme d’installation](installation-mechanism.md).

 

 



