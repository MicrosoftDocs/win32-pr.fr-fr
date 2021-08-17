---
description: Vue d’ensemble de la bibliothèque managée et notes sur l’utilisation de la bibliothèque gérée de plateforme Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Utilisation de la bibliothèque managée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1241787b680045d6c84b440717ced5426e4352d8c280ef58c1bb7f75c9fc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449244"
---
# <a name="using-the-managed-library"></a>Utilisation de la bibliothèque managée

Le common language runtime est la base du .NET Framework Microsoft. Vous pouvez considérer le common language runtime comme un agent qui gère le code au moment de l’exécution, en fournissant des services centraux tels que la gestion de la mémoire, la gestion des threads et la communication à distance, tout en appliquant également une sécurité de code stricte. En fait, le concept de gestion de code est un principe fondamental de la common language runtime. Le code qui cible le common language runtime est connu sous le nom de code managé. Le code qui ne cible pas le common language runtime est connu sous le nom de code natif.

la bibliothèque de classes Framework est une collection complète orientée objet de classes réutilisables que vous pouvez utiliser pour développer des applications allant des applications de ligne de commande traditionnelles ou d’interface utilisateur graphique (GUI) aux applications basées sur les dernières innovations fournies par ASP.NET et les Services Web.

La bibliothèque gérée Tablet PC contient un ensemble d’objets gérés qui étend l’infrastructure pour assurer la prise en charge de l’entrée et de la sortie de l’écriture manuscrite sur Tablet PC, ainsi que l’échange de données avec d’autres ordinateurs.

## <a name="exceptions"></a>Exceptions

Les objets de la bibliothèque managée dans l’API Tablet PC encapsulent les implémentations de la bibliothèque COM. Lorsque l’objet ou le contrôle de bibliothèque COM sous-jacent retourne une erreur, les API managées lèvent une exception Marshal. ThrowExceptionForHR qui fournit les détails sur l’exception COM interne. Vous pouvez faire référence aux valeurs HRESULT dans la référence de la bibliothèque COM pour plus d’informations sur les erreurs pouvant être retournées.

## <a name="object-comparison"></a>Comparaison d’objets

Pour tous les objets de la bibliothèque managée de plateforme Tablet PC, est [**égal**](/previous-versions/windows/) à n’est pas substitué pour comparer correctement deux objets qui sont identiques. L’interface de programmation d’applications (API) managée ne prend pas en charge la comparaison d’égalité d’objets, soit par l’intermédiaire de la fonction **Equals** , soit par le biais de l’opérateur égal (= =).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Liaison avec la dernière Microsoft.Ink.dll

La dernière Microsoft.Ink.dll assembly est un remplacement compatible de Microsoft.Ink.dll version 1,0 et Microsoft.Ink.15.dll. Dans la plupart des cas, vous n’avez pas besoin d’apporter des modifications à vos applications qui sont distribuées avec les anciens assemblys. Toutefois, dans certains cas, vous devez demander à l’common language runtime Loader d’utiliser la bibliothèque de liens dynamiques (DLL) la plus récente, où les anciennes dll ont été référencées.

La seule fois où vous devez effectuer une liaison explicite au nouvel assembly à l’aide de la technique suivante est si votre application utilise un composant qui fait référence à l’assembly version 1,0 ou 1,5 en association avec un composant qui fait référence à un assembly de version plus récent, tel que 1,7, et si ces composants peuvent échanger des données.

La meilleure façon d’indiquer au chargeur common language runtime d’utiliser la DLL la plus récente consiste à rediriger les versions d’assembly au niveau de l’application. Vous pouvez spécifier que votre application utilise la version la plus récente de l’assembly en plaçant des informations de liaison d’assembly dans le fichier de configuration de votre application. Pour plus d’informations sur la redirection des versions d’assembly au niveau de l’application, consultez [redirection des versions d’assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), en particulier la section « Spécification d’une liaison d’assembly dans des fichiers de configuration ».

Vous devrez créer un fichier de configuration dans le même répertoire que votre fichier exécutable. Le fichier de configuration doit porter le même nom que votre exécutable, suivi de l’extension de fichier .config. Par exemple, pour une application, MyApp.exe, le fichier de configuration doit être le fichier MyApp.exe.config. Le fichier de configuration utilise un élément [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) pour forcer toutes les versions antérieures à être mappées à la dernière version, comme illustré dans l’exemple suivant :

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Pour plus d’informations sur les fichiers de configuration, y compris des exemples de construction du Extensible Markup Language (XML) pour le fichier de configuration, consultez [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) et [redirection des versions d’assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

les Applications créées avec microsoft Windows XP Tablet PC Edition Kit de développement 1,7 et versions ultérieures sont automatiquement liées à la nouvelle version de l’assembly Microsoft. Ink. Pour plus d’informations sur la liaison d’assembly, consultez [Comment le runtime localise les assemblys](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> L’utilisation de la stratégie d’application pour effectuer une liaison à l’assembly mis à jour ne fonctionne pas pour les applications qui utilisent la classe [diviseur](/previous-versions/ms583616(v=vs.100)) ou la classe [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Les applications qui utilisent l’une de ces classes doivent continuer à utiliser Microsoft.Ink.15.dll ou être recompilées après avoir fait référence à l’assembly mis à jour.

 

## <a name="working-with-events"></a>Utilisation des événements

Si le code d’un gestionnaire d’événements pour l’un des objets managés lève une exception, l’exception n’est pas remise à l’utilisateur. Pour vous assurer que les exceptions sont remises, utilisez des blocs try-catch dans vos gestionnaires d’événements pour les événements managés.

## <a name="managing-forms"></a>Gestion des formulaires

La classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) et ses classes de base ne définissent pas de finaliseur. Pour nettoyer vos ressources sur un formulaire, écrivez une sous-classe qui fournit un finaliseur (par exemple, le \# destructeur C à l’aide de ~) qui appelle [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1). Pour effectuer le nettoyage, le finaliseur remplace la méthode dispose, puis appelle la méthode dispose de la classe de base. Ne faites pas référence à d’autres objets qui nécessitent la méthode [Finalize](/previous-versions/windows/) dans la méthode dispose lorsque le paramètre Boolean a la **valeur false**, car ces objets ont peut-être déjà été finalisés. Pour plus d’informations sur la libération de ressources [, consultez méthodes Finalize et destructeurs](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Forms et RecognizerContext

Les événements [RecognizerContext](/previous-versions/ms552546(v=vs.100)) s’exécutent dans un thread différent du thread sur lequel se trouve le formulaire. dans Windows Forms, les contrôles sont liés à un thread spécifique et ne sont pas thread-safe. Par conséquent, vous devez utiliser l’une des méthodes Invoke du contrôle pour marshaler l’appel au thread approprié. Quatre méthodes sur un contrôle sont thread-safe : les méthodes [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)et [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) . Pour tous les autres appels de méthode, utilisez l’une de ces méthodes Invoke lors de l’appel à partir d’un thread différent. Pour plus d’informations sur l’utilisation de ces méthodes, consultez [manipulation de contrôles à partir de threads](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>En attente d’événements

L’environnement Tablet PC est multithread. Utilisez la fonction [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) au lieu d’autres méthodes d’attente pour permettre aux appels com (Component Object Model) réentrants d’entrer votre MTA (Multithreaded Apartment) pendant que votre application attend un événement.

## <a name="using-ink-strokes-collections"></a>Utilisation de collections de traits d’encre

Les instances des collections de [traits](/previous-versions/ms552701(v=vs.100)) obtenues à partir d’un objet [Ink](/previous-versions/aa515768(v=msdn.10)) ne sont pas récupérées par le garbage collector. Afin d’éviter une fuite de mémoire, chaque fois que vous utilisez l’une de ces collections, utilisez l’instruction « using », comme indiqué ci-dessous.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Suppression d’objets et de contrôles managés

Pour éviter une fuite de mémoire, vous devez appeler explicitement la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) sur tout objet ou contrôle Tablet PC auquel un gestionnaire d’événements a été attaché avant que l’objet ou le contrôle ne soit hors de portée.

Pour améliorer les performances de votre application, supprimez manuellement les objets, contrôles et collections suivants lorsqu’ils ne sont plus nécessaires.

-   [Séparateur](/previous-versions/ms583616(v=vs.100))
-   [Entrée manuscrite](/previous-versions/aa515768(v=msdn.10))
-   [Collecte](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   [PenInputPanel](/previous-versions/aa514041(v=msdn.10))
-   [RecognizerContext](/previous-versions/ms552546(v=vs.100))
-   [Traits](/previous-versions/ms552701(v=vs.100))

L’exemple C suivant \# illustre certains scénarios dans lesquels la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) est utilisée.


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 