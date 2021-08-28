---
description: Cet exemple montre comment créer un contrôle avec prise en charge de l’écriture manuscrite pour une utilisation dans un navigateur Web. L’exemple utilise l’exemple de formulaire de déclaration automatique d’origine et le transforme en un contrôle qui est placé sur une page Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Exemple de contrôle Web Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe2035028ab622f896489b304ca850db4e25462
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882048"
---
# <a name="ink-web-control-sample"></a>Exemple de contrôle Web Ink

Cet exemple montre comment créer un contrôle avec prise en charge de l’écriture manuscrite pour une utilisation dans un navigateur Web. L’exemple utilise l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md) d’origine et le transforme en un contrôle qui est placé sur une page Web.

Pour plus d’informations sur l’utilisation de l’encre sur le Web, voir [Ink on the Web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Modifications apportées à l’exemple d’origine Project

Cet exemple se compose d’une solution qui inclut deux projets et un fichier HTML. Le premier projet, réclamation, est un projet de bibliothèque de contrôles Microsoft Visual C \# (un contrôle utilisateur). Le code source de ce contrôle est presque identique à celui de l’exemple autoclaims, à deux différences près :

-   `AutoClaims`Dans cet exemple, la classe hérite de la classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) et non de la classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   La classe autoclaims de cet exemple a une méthode publique ajoutée, `DisposeResources` qui supprime les contrôles enfants internes utilisés pour la collecte de l’encre. Cette méthode doit être appelée par thewebpageon que le contrôle est utilisé lorsque cette page est terminée à l’aide du contrôle.

## <a name="referencing-the-control-in-html"></a>Référencement du contrôle en HTML

La solution comprend un fichier HTML, default.htm. Ce fichier est la page vers laquelle le navigateur accède pour charger le contrôle. Le fichier contient une &lt; &gt; balise d’objet qui fait référence au contrôle. Il comprend également un script qui est appelé lorsque la page est déchargée, comme indiqué par la présence de l’attribut OnLoad = " `OnUnload()` " dans &lt; la &gt; balise body. Cette fonction appelle la `DisposeResources` méthode sur le contrôle pour s’assurer que toutes les ressources sont libérées correctement à l’arrêt.


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



Notez le format de la valeur de l’attribut ClassID pour la &lt; &gt; balise Object. Il nomme l’assembly, suivi d’un \# séparateur de signe, puis de l’espace de noms qui contient le contrôle, puis du nom de classe du contrôle.

Un contrôle utilisateur réel inclut probablement des méthodes supplémentaires utilisées pour conserver ou envoyer les données collectées dans l’application.

## <a name="the-autoclaims_webcontrol-project"></a>Le Project WebControl de la récupération d’autorevendication \_

le projet de contrôle de configuration de l’autorevendication \_ est un Project de déploiement qui crée un programme d’installation qui ajoute une racine virtuelle, \_ le contrôle de l’utilisateur sur le serveur Web lors de l’installation. Le contrôle et le fichier HTML sont placés dans cette racine virtuelle.

> [!Note]  
> Les exemples Web compilés ne sont pas installés par l’option d’installation par défaut pour le kit de développement logiciel (SDK). Vous devez effectuer une installation personnalisée et sélectionner la sous-option « exemples Web précompilés » pour les installer.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de formulaire de déclaration automatique](auto-claims-form-sample.md)
</dt> <dt>

[Entrée manuscrite sur le Web](ink-on-the-web.md)
</dt> </dl>

 

 
