---
description: Une bibliothèque de liens dynamiques (DLL) est un module qui contient des fonctions et des données qui peuvent être utilisées par un autre module (application ou DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Bibliothèques de Dynamic-Link (bibliothèques de liens dynamiques)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369091464aad63ea78ea9f24a84fb4eb49eb810a1faff14571fc67e2e39bb0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815898"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Bibliothèques de Dynamic-Link (bibliothèques de liens dynamiques)

Une *bibliothèque de liens dynamiques* (dll) est un module qui contient des fonctions et des données qui peuvent être utilisées par un autre module (application ou dll).

Une DLL peut définir deux types de fonctions : exporté et interne. Les fonctions exportées sont destinées à être appelées par d’autres modules, ainsi qu’à partir de la DLL dans laquelle elles sont définies. Les fonctions internes sont généralement destinées à être appelées uniquement à partir de la DLL dans laquelle elles sont définies. Bien qu’une DLL puisse exporter des données, ses données sont généralement utilisées uniquement par ses fonctions. Toutefois, rien n’empêche un autre module de lire ou d’écrire cette adresse.

Les dll offrent un moyen de modulariser les applications afin que leurs fonctionnalités puissent être mises à jour et réutilisées plus facilement. Les dll permettent également de réduire la surcharge de mémoire lorsque plusieurs applications utilisent la même fonctionnalité en même temps, car même si chaque application reçoit sa propre copie des données DLL, les applications partagent le code DLL.

l’interface de programmation d’applications (api) Windows est implémentée sous la forme d’un ensemble de dll, de sorte que tout processus qui utilise l’API Windows utilise la liaison dynamique.

-   [À propos des bibliothèques Dynamic-Link](about-dynamic-link-libraries.md)
-   [Utilisation des bibliothèques de Dynamic-Link](using-dynamic-link-libraries.md)
-   [Référence de bibliothèque de liens dynamiques](dynamic-link-library-reference.md)

> [!Note]  
> Si vous êtes un utilisateur rencontrant des difficultés avec une DLL sur votre ordinateur, vous devez contacter le support technique de l’éditeur du logiciel qui publie la DLL. si vous pensez que vous avez besoin de la prise en charge d’un produit Microsoft (y compris Windows), accédez à notre site de support technique à l’adresse [support.microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Dll (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
