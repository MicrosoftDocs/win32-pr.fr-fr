---
title: Implémentation de CSearch
description: Implémentation de CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- plug-ins Lecteur Windows Media, classe CSearch
- plug-ins, classe CSearch
- plug-ins d’interface utilisateur, classe CSearch
- Plug-ins d’interface utilisateur, classe CSearch
- CSearch, classe
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f99f3e232d11075bde9905169099649a3b6e754454ac10af60b8a83493fcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748154"
---
# <a name="implementing-csearch"></a>Implémentation de CSearch

l’interface **IWMPPluginUI** a plusieurs méthodes qui sont appelées par Lecteur Windows Media à des moments différents pendant le cycle de vie d’une instance de plug-in. L’Assistant fournit des implémentations de base de ces méthodes, ainsi que le constructeur de classe et le destructeur, ainsi que d’autres méthodes de classe. le fichier Search. h doit être modifié de sorte que Lecteur Windows Media puisse communiquer avec l’interface utilisateur, ce qui est décrit dans la section suivante.

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

 

 




