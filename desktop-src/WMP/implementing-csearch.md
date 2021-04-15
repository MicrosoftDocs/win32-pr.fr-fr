---
title: Implémentation de CSearch
description: Implémentation de CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Plug-ins du lecteur Windows Media, classe CSearch
- plug-ins, classe CSearch
- plug-ins d’interface utilisateur, classe CSearch
- Plug-ins d’interface utilisateur, classe CSearch
- CSearch, classe
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507131"
---
# <a name="implementing-csearch"></a>Implémentation de CSearch

L’interface **IWMPPluginUI** possède plusieurs méthodes qui sont appelées par le lecteur Windows Media à des moments différents pendant le cycle de vie d’une instance de plug-in. L’Assistant fournit des implémentations de base de ces méthodes, ainsi que le constructeur de classe et le destructeur, ainsi que d’autres méthodes de classe. Le fichier Search. h doit être modifié de sorte que le lecteur Windows Media puisse communiquer avec l’interface utilisateur, ce qui est décrit dans la section suivante.

Pour que la classe CPluginWindow ait accès à la variable de membre privé m \_ Core, une déclaration de classe Friend doit être effectuée à l’intérieur de la définition de la classe CSearch, comme indiqué dans l’extrait de code suivant :


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation de plug-ins d’interface utilisateur**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




