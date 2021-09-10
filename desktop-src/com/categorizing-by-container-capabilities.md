---
title: Catégorisation par fonctionnalités de conteneur
description: Les composants requièrent souvent certaines fonctionnalités du conteneur et ne fonctionnent pas avec un conteneur qui ne fournit pas la prise en charge.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363543"
---
# <a name="categorizing-by-container-capabilities"></a>Catégorisation par fonctionnalités de conteneur

Les composants requièrent souvent certaines fonctionnalités du conteneur et ne fonctionnent pas avec un conteneur qui ne fournit pas la prise en charge. L’interface utilisateur doit filtrer les composants qui requièrent des fonctionnalités que le conteneur ne prend pas en charge. Pour ce faire, les composants peuvent être catégorisés par la fonctionnalité de conteneur requise.

Voici un exemple de composants qui requièrent des fonctionnalités du conteneur et qui ne fonctionnent pas dans les conteneurs qui ne prennent pas en charge cette fonctionnalité. il s’agit de contrôles OLE Frame simples. La catégorisation par fonctionnalités de conteneur est effectuée par une clé de Registre supplémentaire au sein de la clé CLSID du composant :

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Comme indiqué dans cet exemple, un composant peut appartenir à des catégories de composants qui indiquent les fonctionnalités prises en charge ainsi que les catégories de composants qui indiquent les fonctionnalités requises.

Dans l’exemple suivant, le contrôle Button est un contrôle OLE générique qui ne prend pas en charge les fonctionnalités supplémentaires. Elle fonctionnera dans n’importe quel conteneur de contrôle OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

comparez l’exemple précédent à l’exemple suivant dans lequel le MyDBControl peut utiliser Visual Basic la liaison de données si le conteneur le prend en charge. toutefois, il a été défini de manière à fonctionner dans des conteneurs qui ne prennent pas en charge la liaison de données Visual Basic (par exemple, une API de base de données différente) :

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

Le contrôle GroupBox est un contrôle Frame simple. Il s’appuie sur le conteneur qui implémente l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) et fonctionnera correctement uniquement dans ces conteneurs :

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

un conteneur qui prend en charge Visual Basic contrôles liés aux données mais ne prend pas en charge les contrôles frame simples qui spécifient \_ le contrôle catid et \_ le catid VBDatabound à l’interface utilisateur du contrôle insert. La liste de contrôles affichée à l’utilisateur doit contenir le \_ bouton CLSID et le CLSID \_ MyDBControl. Le \_ GroupBox CLSID ne s’affiche pas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Association d’icônes à une catégorie](associating-icons-with-a-category.md)
</dt> <dt>

[Catégorisation par fonctionnalités de composant](categorizing-by-component-capabilities.md)
</dt> <dt>

[Classes et associations par défaut](default-classes-and-associations.md)
</dt> <dt>

[Définition des catégories de composants](defining-component-categories.md)
</dt> <dt>

[Gestionnaire de catégories de composants](the-component-categories-manager.md)
</dt> </dl>

 

 




