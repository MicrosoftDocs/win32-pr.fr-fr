---
title: Demande d’un objet pour une interface
description: Demande d’un objet pour une interface
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a173342c7dba59c09cdef05c6b20d9d4d37da9d6971e6a7c26c1787b708121bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680736"
---
# <a name="asking-an-object-for-an-interface"></a>Demande d’un objet pour une interface

Nous avons vu précédemment qu’un objet peut implémenter plus d’une interface. L’objet de boîte de dialogue élément commun est un exemple réel de cette. Pour prendre en charge les utilisations les plus courantes, l’objet implémente l’interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Cette interface définit les méthodes de base pour afficher la boîte de dialogue et obtenir des informations sur le fichier sélectionné. Pour une utilisation plus avancée, toutefois, l’objet implémente également une interface nommée [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Un programme peut utiliser cette interface pour personnaliser l’apparence et le comportement de la boîte de dialogue en ajoutant de nouveaux contrôles d’interface utilisateur.

Rappelez-vous que chaque interface COM doit hériter, directement ou indirectement, de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Le diagramme suivant montre l’héritage de l’objet de boîte de dialogue d’élément commun.

![diagramme qui affiche des interfaces exposées par l’objet de boîte de dialogue d’élément commun](images/com06.png)

Comme vous pouvez le voir dans le diagramme, l’ancêtre direct de [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) est l’interface [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , qui à son tour hérite de [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). À mesure que vous remontez la chaîne d’héritage de **IFileOpenDialog** à **IModalWindow**, les interfaces définissent la fonctionnalité de fenêtre généralisée de plus en plus généralisée. Enfin, l’interface **IModalWindow** hérite de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). L’objet de boîte de dialogue d’élément commun implémente également [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), qui existe dans une chaîne d’héritage distincte.

Supposons à présent que vous avez un pointeur vers l’interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Comment obtenir un pointeur vers l’interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?

![diagramme qui montre deux pointeurs d’interface vers des interfaces sur le même objet](images/com07.png)

Le simple cast du pointeur [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) vers un pointeur [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ne fonctionnera pas. Il n’existe pas de méthode fiable pour « effectuer un cast croisé » dans une hiérarchie d’héritage, sans une forme d’informations de type au moment de l’exécution (RTTI), qui est une fonctionnalité qui dépend fortement de la langue.

L’approche COM consiste à *demander* à l’objet de vous fournir un pointeur [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , en utilisant la première interface comme canal dans l’objet. Pour ce faire, appelez la méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) à partir du premier pointeur d’interface. Vous pouvez considérer **QueryInterface** comme une version indépendante du langage du mot clé **Dynamic \_ Cast** en C++.

La méthode [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) a la signature suivante :

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

En fonction de ce que vous connaissez déjà [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), vous pouvez être en mesure de deviner le fonctionnement de [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

-   Le paramètre *riid* est le GUID qui identifie l’interface que vous demandez. Le type de données **REFIID** est un **typedef** pour `const GUID&` . Notez que l’identificateur de classe (CLSID) n’est pas requis, car l’objet a déjà été créé. Seul l’identificateur d’interface est nécessaire.
-   Le paramètre *ppvObject* reçoit un pointeur vers l’interface. Le type de données de ce paramètre **est \* \* void**, pour la même raison que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilise ce type de données : [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) peut être utilisé pour interroger une interface com, de sorte que le paramètre ne peut pas être fortement typé.

Voici comment appeler [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour recevoir un pointeur [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



Comme toujours, vérifiez la valeur de retour **HRESULT** , en cas d’échec de la méthode. Si la méthode réussit, vous devez appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quand vous avez fini d’utiliser le pointeur, comme décrit dans [gestion de la durée de vie d’un objet](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Suivant

[Allocation de mémoire dans COM](memory-allocation-in-com.md)

 

 