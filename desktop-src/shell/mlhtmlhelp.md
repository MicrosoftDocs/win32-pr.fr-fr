---
description: Affiche une fenêtre d’aide qui correspond au paramètre de langue de l’interface utilisateur actuel.
title: MLHtmlHelp, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: c38e84df2ca6f379e7d479125f1f454a10426406ba40ad21721fe01f67cce6f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090209"
---
# <a name="mlhtmlhelp-function"></a>MLHtmlHelp, fonction

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Affiche une fenêtre d’aide qui correspond au paramètre de langue de l’interface utilisateur actuel.

## <a name="syntax"></a>Syntaxe


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndCaller* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre parente qui appelle cette fonction.

</dd> <dt>

*pszFile* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers une mémoire tampon qui contient le chemin d’accès complet d’un fichier d’aide compilé (. chm) ou un fichier de rubrique dans un fichier d’aide spécifié.

</dd> <dt>

*uCommand* \[ dans\]
</dt> <dd>

Type : **uint**

Commande à exécuter. Cette fonction prend directement en charge uniquement la [ \_ \_ rubrique d’affichage HH](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) et le [ \_ \_ texte affiché \_ hh](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command). Dans le cas d’une autre commande, l’appel est transféré sans la valeur *dwCrossCodePage* à [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).

</dd> <dt>

*dwData* \[ dans\]
</dt> <dd>

Type : **\_ ptr DWORD**

Toutes les données qui peuvent être requises, en fonction de la valeur du paramètre *uCommand* .

</dd> <dt>

*dwCrossCodePage* \[ dans\]
</dt> <dd>

Type : **DWORD**

Valeur **DWORD** indiquant la page de codes du paramètre de langue actuelle de l’interface utilisateur, par exemple CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HWND**

Selon le *uCommand* spécifié et le résultat, **MLHtmlHelp** retourne l’un des éléments suivants, ou les deux :

-   Handle (HWND) de la fenêtre d’aide.
-   **Valeur null**. Dans certains cas, **null** indique un échec ; dans d’autres cas, la **valeur null** indique que la fenêtre d’aide n’a pas encore été créée.

## <a name="remarks"></a>Remarques

Si un problème se produit avec le chemin d’accès du fichier d’aide pour la langue actuelle, l’appel est transféré à [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) pour la gestion standard.

Lorsque la fenêtre d’aide est fermée, le focus revient au propriétaire, sauf si le propriétaire est le bureau. Si *hwndCaller* est le bureau, le système d’exploitation détermine où le focus est retourné.

En outre, si **MLHtmlHelp** envoie des messages de notification à partir de la fenêtre d’aide, les messages sont envoyés à *hwndCaller* tant que vous avez activé le suivi des [messages de notification](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) dans la définition de la fenêtre d’aide.

## <a name="examples"></a>Exemples

L’exemple suivant appelle la commande [hh \_ Display \_ topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) pour ouvrir le fichier d’aide nommé Help. chm et afficher sa rubrique par défaut dans la fenêtre d’aide nommée `Mainwin` . En règle générale, la fenêtre d’aide spécifiée dans cette commande est une [visionneuse d’aide HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)standard.

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Quand vous utilisez cette fonction, définissez la taille de la pile de l’exécutable d’hébergement sur au moins 100 000. Si la taille de la pile définie est trop petite, le thread créé pour exécuter l’aide HTML est également créé avec cette taille de pile, et l’opération peut échouer. Si vous le souhaitez, vous pouvez supprimer/STACK de la ligne de commande de liaison et supprimer tous les paramètres de pile dans le fichier DEF de l’exécutable (la taille de la pile par défaut est de 1 Mo dans le cas présent). Vous pouvez également définir la taille de la pile à l’aide de la commande du compilateur/fnumber (le compilateur passera ce à l’éditeur de liens en tant que/STACK).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **MLHtmlHelpW** (Unicode) et **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
