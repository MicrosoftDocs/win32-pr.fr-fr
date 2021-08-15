---
description: Cette rubrique explique comment implémenter un composant en tant que bibliothèque de liens dynamiques (DLL) dans Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Fonctions DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8c10951c63e14656fa967693145444c5d5fbffd96a2b11fa9ae4201ac89ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821083"
---
# <a name="dll-functions"></a>Fonctions DLL

Cette rubrique explique comment implémenter un composant en tant que bibliothèque de liens dynamiques (DLL) dans Microsoft DirectShow.

Une DLL doit implémenter les fonctions suivantes pour qu’elle puisse être inscrite, désinscrite et chargée en mémoire.

-   [*DllMain*](/windows/desktop/Dlls/dllmain): point d’entrée de la dll. Le nom *DllMain* est un espace réservé pour le nom de la fonction définie par la bibliothèque. l’implémentation de DirectShow utilise le nom **DllEntryPoint**. Pour plus d’informations, consultez le kit de développement Platform SDK.
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): crée une instance de fabrique de classe. Décrit dans les sections précédentes.
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): interroge si la dll peut être déchargée en toute sécurité.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crée des entrées de Registre pour la dll.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): supprime les entrées de Registre pour la dll.

Parmi celles-ci, les trois premières sont implémentées par DirectShow. Si votre modèle de fabrique fournit une fonction d’initialisation dans la variable membre [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) , cette fonction est appelée depuis l’intérieur de la fonction de point d’entrée de la dll. Pour plus d’informations sur le moment où le système appelle la fonction de point d’entrée DLL, consultez [*DllMain*](/windows/desktop/Dlls/dllmain).

vous devez implémenter [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), mais DirectShow fournit une fonction nommée [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) qui effectue les tâches nécessaires. Votre composant peut simplement encapsuler cette fonction, comme illustré dans l’exemple suivant :


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



Toutefois, dans [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) , vous pouvez personnaliser le processus d’inscription en fonction des besoins. Si votre DLL contient un filtre, vous devrez peut-être effectuer des tâches supplémentaires. pour plus d’informations, consultez [comment inscrire des filtres de DirectShow](how-to-register-directshow-filters.md).

Dans votre fichier de définition de module (. def), exportez toutes les fonctions DLL à l’exception de la fonction de point d’entrée. Voici un exemple de fichier. def :


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Vous pouvez inscrire la DLL à l’aide de l’utilitaire Regsvr32.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[comment créer une DLL de filtre DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
