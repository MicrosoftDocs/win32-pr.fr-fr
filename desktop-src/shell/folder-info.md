---
description: La section obtenir l’ID d’un dossier a présenté deux approches pour obtenir le pointeur d’un objet Namespace vers une liste d’identificateurs d’éléments (PIDL).
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: Obtention d’informations sur le contenu d’un dossier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991065"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>Obtention d’informations sur le contenu d’un dossier

La section [obtenir l’ID d’un dossier a](folder-id.md) présenté deux approches pour obtenir le pointeur d’un objet Namespace vers une liste d’identificateurs d’éléments (PIDL). Une question évidente est : une fois que vous avez un PIDL, que pouvez-vous en faire ? Une question associée est : que se passe-t-il si aucune de ces approches ne fonctionne ou convient à votre application ? La réponse aux deux questions requiert un examen plus approfondi de l’implémentation de l’espace de noms. La clé est l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

-   [Utilisation de l’interface IShellFolder](#using-the-ishellfolder-interface)
-   [Énumération du contenu d’un dossier](#enumerating-the-contents-of-a-folder)
-   [Détermination des noms d’affichage et d’autres propriétés](#determining-display-names-and-other-properties)
-   [Obtention d’un pointeur vers l’interface IShellFolder d’un sous-dossier](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [Détermination du dossier parent d’un objet](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>Utilisation de l’interface IShellFolder

Plus haut dans cette documentation, les dossiers d’espace de noms étaient appelés objets. Bien que, à ce stade, le terme était utilisé dans un sens faible, il s’agit en fait d’un bon sens. Chaque dossier d’espace de noms est représenté par un objet COM (Component Object Model). Chaque objet Folder expose un certain nombre d’interfaces qui peuvent être utilisées pour un large éventail de tâches. Certaines interfaces facultatives ne peuvent pas être exposées par tous les dossiers. Toutefois, tous les dossiers doivent exposer l’interface fondamentale, [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).

La première étape de l’utilisation d’un objet Folder consiste à récupérer un pointeur vers son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . En plus de fournir l’accès aux autres interfaces de l’objet, **IShellFolder** expose un groupe de méthodes qui gèrent un certain nombre de tâches courantes, dont plusieurs sont décrites dans cette section.

Pour récupérer un pointeur vers l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) d’un objet Namespace, vous devez d’abord appeler [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder). Cette fonction retourne un pointeur vers l’interface **IShellFolder** de la racine de l’espace de noms, le bureau. Une fois que vous disposez de l’interface **IShellFolder** du bureau, vous pouvez procéder de différentes façons.

Si vous avez déjà le PIDL du dossier qui vous intéresse (par exemple, en appelant [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)), vous pouvez récupérer son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) en appelant la méthode [**IShellFolder :: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) du bureau. Si vous avez le chemin d’accès d’un objet de système de fichiers, vous devez d’abord obtenir son PIDL en appelant la méthode [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) du bureau, puis appeler **IShellFolder :: BindToObject**. Si aucune de ces approches n’est applicable, vous pouvez utiliser d’autres méthodes **IShellFolder** pour naviguer dans l’espace de noms. Pour plus d’informations, consultez [navigation dans l’espace de noms](navigate.md).

## <a name="enumerating-the-contents-of-a-folder"></a>Énumération du contenu d’un dossier

La première chose que vous souhaitez généralement faire avec un dossier est de savoir ce qu’il contient. Vous devez d’abord appeler la méthode [**IShellFolder :: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) du dossier. Le dossier crée un objet énumération OLE standard et retourne son interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) . Cette interface expose quatre méthodes standard ([**clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone), [**suivant**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next), [**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)et [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)) qui peuvent être utilisées pour énumérer le contenu du dossier.

La procédure de base pour énumérer le contenu d’un dossier est la suivante :

1.  Appelez la méthode Folders [**IShellFolder :: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) pour récupérer un pointeur vers l’interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) d’un objet d’énumération.
2.  Transmettez un PIDL non alloué à [**IEnumIDList :: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). **Ensuite** , s’occupe de l’allocation de PIDL, mais l’application doit la désallouer lorsqu’elle n’est plus nécessaire. Lors du retour **suivant** , le PIDL contient uniquement l’ID d’élément de l’objet et les caractères **null** de fin. En d’autres termes, il s’agit d’un PIDL à un seul niveau, par rapport au dossier, et non d’un PIDL complet.
3.  Répétez l’étape 2 jusqu’à ce que [**Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) retourne S \_ false pour indiquer que tous les éléments ont été énumérés.
4.  Appelez **IEnumIDList :: Release** pour libérer l’objet d’énumération.

> [!Note]  
> Il est important de suivre si vous utilisez un PIDL complet ou relatif. Certaines fonctions et méthodes acceptent les deux, mais d’autres n’en prennent que l’un ou l’autre.

 

Les trois méthodes [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) restantes ([**Réinitialiser**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset), [**Ignorer**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)et [**cloner**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) sont utiles si vous devez effectuer des énumérations répétées du dossier. Elles vous permettent de réinitialiser l’énumération, d’ignorer un ou plusieurs objets et de faire une copie de l’objet d’énumération pour conserver son état.

## <a name="determining-display-names-and-other-properties"></a>Détermination des noms d’affichage et d’autres propriétés

Une fois que vous avez énuméré tous les PIDL contenus dans un dossier, vous pouvez déterminer le type d’objets qu’ils représentent. L’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) fournit un certain nombre de méthodes utiles, dont deux sont décrites ici. D’autres méthodes **IShellFolder** et d’autres interfaces de dossiers Shell sont abordées plus loin.

L’une des propriétés les plus utiles est le nom complet de l’objet. Pour récupérer le nom complet d’un objet, transmettez son PIDL à [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Bien que l’objet puisse être situé n’importe où sous le dossier parent dans l’espace de noms, son PIDL doit être relatif au dossier.

[**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) retourne le nom complet dans le cadre d’une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Étant donné que l’extraction du nom complet à partir d’une structure **STRRET** peut être un peu délicate, l’interpréteur de commandes fournit deux fonctions qui effectuent le travail pour vous, [**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) et [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa). Les deux fonctions prennent une structure **STRRET** et retournent le nom complet sous la forme d’une chaîne normale. Elles diffèrent uniquement par la façon dont la chaîne est allouée.

En plus de son nom complet, un objet peut avoir un certain nombre d’attributs, par exemple s’il s’agit d’un dossier ou s’il peut être déplacé. Vous pouvez récupérer les attributs d’un objet en passant son PIDL à [**IShellFolder :: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof). La liste complète des attributs est assez volumineuse. vous devez donc voir la référence pour plus d’informations. Notez que le PIDL que vous transmettez à **GetAttributesOf** doit être de niveau simple. En particulier, **IShellFolder :: GetAttributesOf** accepte le PIDL retourné par [**IEnumIDList :: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). Vous pouvez passer un tableau de PIDL et **GetAttributesOf** retournera les attributs que tous les objets du tableau ont en commun.

Si vous avez le chemin qualifié complet d’un objet ou PIDL, [**SHGetFileInfo**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) offre un moyen simple de récupérer des informations sur un objet qui est suffisant pour de nombreuses raisons. **SHGetFileInfo** prend un chemin d’accès qualifié complet ou PIDL, et retourne une variété d’informations sur l’objet, notamment :

-   Nom complet de l’objet
-   Attributs de l’objet
-   Gère les icônes de l’objet
-   Handle de la liste d’images système
-   Chemin d’accès du fichier contenant l’icône de l’objet

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>Obtention d’un pointeur vers l’interface IShellFolder d’un sous-dossier

Vous pouvez déterminer si votre dossier contient des sous-dossiers en appelant [**IShellFolder :: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) et en vérifiant si l' \_ indicateur de dossier SFGAO est défini. Si un objet est un dossier, vous pouvez y créer une liaison, qui vous fournit un pointeur vers son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Pour effectuer une liaison à un sous-dossier, appelez la méthode [**IShellFolder :: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) du dossier parent. Cette méthode prend le PIDL du sous-dossier et retourne un pointeur vers son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Une fois que vous avez ce pointeur, vous pouvez utiliser les méthodes **IShellFolder** pour énumérer le contenu des sous-dossiers, déterminer leurs propriétés, et ainsi de suite.

## <a name="determining-an-objects-parent-folder"></a>Détermination du dossier parent d’un objet

Si vous avez le PIDL d’un objet, vous pouvez avoir besoin d’un handle vers l’une des interfaces exposées par son dossier parent. Par exemple, si vous souhaitez déterminer le nom complet associé à un PIDL à l’aide de [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), vous devez d’abord récupérer l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du parent de l’objet. Il est possible de le faire avec les techniques décrites dans les sections précédentes. Toutefois, une approche bien plus simple consiste à utiliser la fonction Shell, [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent). Cette fonction prend le PIDL complet d’un objet et retourne un pointeur d’interface spécifié sur le dossier parent. Éventuellement, elle retourne également le PIDL à un seul niveau de l’élément pour une utilisation dans des méthodes telles que [**IShellFolder :: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).

L’exemple d’application console suivant récupère le PIDL du dossier spécial du système et retourne son nom complet.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



L’application utilise d’abord [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) pour récupérer le PIDL du dossier système. Il appelle ensuite [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent), qui retourne un pointeur vers l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du dossier parent et le PIDL du dossier système par rapport à son parent. Il utilise ensuite la méthode [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) du dossier parent pour récupérer le nom complet du dossier système. Étant donné que **GetDisplayNameOf** retourne une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) est utilisé pour convertir le nom complet en une chaîne normale. Une fois le nom complet affiché, les pointeurs d’interface sont libérés et le système PIDL libéré. Notez que vous ne devez pas libérer le PIDL relatif retourné par **SHBindToParent**.

 

 
