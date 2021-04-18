---
description: Vous pouvez installer des produits entiers avec des fonctions de Windows Installer. Les étapes suivantes décrivent l’installation d’un produit.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installation d’une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519508"
---
# <a name="installing-an-application"></a>Installation d’une application

Vous pouvez installer des produits entiers avec des fonctions de Windows Installer. Les étapes suivantes décrivent l’installation d’un produit.

**Pour installer un produit**

1.  Exécutez un produit par le biais de sa séquence d’installation ou de désinstallation en appelant la fonction [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .
2.  Spécifiez le niveau d’installation en appelant la fonction [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .

    Vous pouvez utiliser les paramètres de la fonction [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) pour définir l’état d’installation. Par exemple, vous pouvez définir l’État sur installer localement ou pour installer à partir de la source. Vous pouvez définir la plage de fonctionnalités du produit à inclure en définissant le niveau.

Pour plus d’informations sur l’installation d’une application, consultez [résilience](resiliency.md) et [mécanisme d’installation](installation-mechanism.md).

 

 



