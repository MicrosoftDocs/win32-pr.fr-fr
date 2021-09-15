---
description: IShellDispatch2. ShellExecute, méthode-effectue une opération spécifiée sur un fichier spécifié.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: IShellDispatch2. ShellExecute, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412467"
---
# <a name="ishelldispatch2shellexecute-method"></a>IShellDispatch2. ShellExecute, méthode

Exécute une opération spécifiée sur un fichier spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sFile* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient le nom du fichier sur lequel **ShellExecute** effectue l’action spécifiée par *vOperation*.

</dd> <dt>

*vArguments* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Chaîne qui contient les valeurs des paramètres de l’opération.

</dd> <dt>

*vDirectory* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Chemin d’accès complet du répertoire qui contient le fichier spécifié par *sFile*. Si ce paramètre n’est pas spécifié, le répertoire de travail actuel est utilisé.

</dd> <dt>

*vOperation* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Opération à effectuer. Cette valeur est définie sur l’une des chaînes de verbe qui est prise en charge par le fichier. Pour plus d’informations sur les verbes, consultez la section Notes. Si ce paramètre n’est pas spécifié, l’opération par défaut est effectuée.

</dd> <dt>

*vShow* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Recommandation relative à l’affichage initial de la fenêtre d’application. L’application peut ignorer cette recommandation. Ce paramètre peut prendre les valeurs suivantes. Si ce paramètre n’est pas spécifié, l’application utilise sa valeur par défaut.



| Valeur                                                                                                                               | Signification                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Ouvrez l’application à l’aide d’une fenêtre masquée.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Ouvrez l’application avec une fenêtre normale. Si la fenêtre est réduite ou agrandie, le système la restaure à sa taille et à sa position d’origine.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Ouvrez l’application avec une fenêtre réduite.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Ouvrez l’application avec une fenêtre agrandie.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Ouvre l’application avec sa fenêtre à sa taille et à sa position les plus récentes. La fenêtre active reste active.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Ouvre l’application avec sa fenêtre à sa taille et à sa position actuelles.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Ouvrez l’application avec une fenêtre réduite. La fenêtre active reste active.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Ouvre l’application avec sa fenêtre dans l’État par défaut spécifié par l’application.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ShellExecute**](./shell-shellexecute.md) .

Cette méthode est équivalente au lancement de l’une des commandes associées au menu contextuel d’un fichier. Chaque commande est représentée par une chaîne de verbe. L’ensemble des verbes pris en charge varie d’un fichier à un fichier. Le verbe le plus couramment pris en charge est « Open », qui est généralement le verbe par défaut. Les autres verbes peuvent être pris en charge uniquement par certains types de fichiers. Pour plus d’informations sur les verbes de Shell, consultez [lancement d’applications](launch.md) ou [extension des menus contextuels](context.md).

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation de **ShellExecute** pour ouvrir Bloc-notes. l’utilisation est indiquée pour JScript et VBScript.

JScript :


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
