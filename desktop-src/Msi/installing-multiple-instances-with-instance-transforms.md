---
description: Cette rubrique fournit des instructions pour l’installation ou la réinstallation d’une installation de plusieurs instances qui utilise des transformations d’instance.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installation de plusieurs instances à l’aide de transformations d’instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a25b2cba8fd91316d62692d278345e0f7d9751f018e1c33239412988bfe118a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074899"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Installation de plusieurs instances à l’aide de transformations d’instance

Cette rubrique fournit des instructions pour l’installation ou la réinstallation d’une installation de plusieurs instances qui utilise des transformations d’instance.

-   Lors de l’installation d’une nouvelle instance avec une transformation d’instance, incluez la propriété **MSINEWINSTANCE** et définissez **MSINEWINSTANCE**= 1.
-   Lors de l’installation d’une nouvelle instance de à l’aide d’une transformation d’instance, incluez la propriété transformations et définissez la première transformation de la liste des transformations sur la transformation d’instance qui modifie le code du produit. Toutes les transformations de personnalisation doivent suivre la transformation d’instance au début de cette liste.
-   Le moyen le plus simple d’effectuer une installation de maintenance et de réinstaller une instance consiste à faire référence au code de produit de l’instance. Si vous lancez l’installation de maintenance à l’aide du chemin d’accès au package, vous devez également spécifier le code de produit de l’instance. À partir de la ligne de commande, utilisez l’option/n {Product Code}. À partir du code ou du script, utilisez la propriété **MSIINSTANCEGUID** .

L’exemple suivant montre comment installer une nouvelle instance à partir d’une ligne de commande dans laquelle la transformation d’instance est précédée d’un signe deux-points qui spécifie que la transformation est incorporée dans le package.

**msiexec/I mypackage.msi transformations = : instance. MST MSINEWINSTANCE = 1/QB**

L’exemple suivant illustre l’installation d’une nouvelle instance de à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

L’exemple suivant illustre l’installation de la nouvelle instance à partir d’un script.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

L’exemple suivant réinstalle une instance sans remettre en cache le package. L’instance est référencée par son code de produit {00000001-0002-0000-0000-624474736554} .

**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**

L’exemple suivant réinstalle une instance et met à nouveau le package à partir de la ligne de commande. L’instance est référencée par le chemin d’accès au package. Vous devez uniquement inclure l’option/n {Product Code} si le produit est installé à l’origine avec une transformation d’instance.

**msiexec/I c : \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/QB**

L’exemple suivant réinstalle une instance de et met en cache le package à l’aide de **MsiInstallProduct**. L’instance est référencée par le chemin d’accès au package. Utilisez la propriété **MSIINSTANCEGUID** pour fournir le code de produit de l’instance.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

L’exemple suivant réinstalle une instance de et met en cache le package à l’aide d’un script. Utilisez la propriété **MSIINSTANCEGUID** pour fournir le code de produit de l’instance.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

L’exemple suivant montre comment publier une instance à l’aide de la ligne de commande.

**msiexec/JM mypackage.msi/t : instance. MST/c/QB**

L’exemple suivant montre comment installer pour publier une instance à l’aide de **MsiAdvertiseProductEx**.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

L’exemple suivant montre comment appliquer un correctif à une instance à partir d’une ligne de commande. Vous devez uniquement inclure l’option/n {Product Code} si le produit a été installé à l’origine avec une transformation d’instance.

**msiexec/p mypatch. msp/n {00000001-0002-0000-0000-624474736554} /qb**

L’exemple suivant montre comment appliquer un correctif à une installation d’instance à l’aide de [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md) et [création de plusieurs instances à l’aide de transformations d’instance](authoring-multiple-instances-with-instance-transforms.md).

 

 



