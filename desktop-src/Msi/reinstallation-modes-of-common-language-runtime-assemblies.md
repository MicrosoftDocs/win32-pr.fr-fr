---
description: Les assemblys Common Language Runtime qui sont installés dans le Global Assembly Cache doivent avoir des fichiers identiques dans toutes les occurrences de l’assembly.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modes de réinstallation des assemblys du Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021274"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Modes de réinstallation des assemblys du Common Language Runtime

Les assemblys Common Language Runtime qui sont installés dans le Global Assembly Cache doivent avoir des fichiers identiques dans toutes les occurrences de l’assembly. Cela signifie que les modes de réinstallation utilisés par [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) et [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) doivent avoir des significations différentes pour les composants normaux et les assemblys de Common Language Runtime. Les définitions de modes de réinstallation suivantes s’appliquent aux assemblys common language runtime.



| Mode de réinstallation                  | Signification pour les composants Microsoft .NET                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| REINSTALLMODE \_ FILEMISSING      | Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.                                         |
| REINSTALLMODE \_ FILEOLDERVERSION | Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.                                         |
| REINSTALLMODE \_ FILEEQUALVERSION | Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.                                         |
| REINSTALLMODE \_ FILEEXACT        | Installez ou réinstallez le composant common language runtime s’il est manquant ou incomplet.                                         |
| REINSTALLMODE \_ FILEVERIFY       | Installez ou réinstallez le composant common language runtime s’il est manquant ou si le composant existant est incomplet ou endommagé. |
| REINSTALLMODE \_ FILEREPLACE      | Installez ou réinstallez toujours le composant common language runtime.                                                                 |



 

 

 



