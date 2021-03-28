---
description: Effectue une opération sur un fichier spécifié.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 841c30be827ddabc40bd8af50423c844ce927e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524428"
---
# <a name="wowshellexecute-function"></a>WOWShellExecute fonction)

\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Effectue une opération sur un fichier spécifié. **WOWShellExecute** existe uniquement pour une utilisation avec la machine DOS virtuelle Microsoft Windows NT (Ntvdm.exe), qui permet d’exécuter le système d’exploitation sur disque (dos) et le logiciel 16 bits sur un système Windows, et ne doit pas être utilisé par une autre personne. Utilisez à la place [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="syntax"></a>Syntaxe


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre propriétaire utilisée pour afficher une interface utilisateur ou des messages d’erreur. Cette valeur peut être **null** si l’opération n’est pas associée à une fenêtre.

</dd> <dt>

*lpOperation* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers une chaîne se terminant par un caractère **null**, référencé dans ce cas en tant que *verbe*, qui spécifie l’action à exécuter. L’ensemble des verbes disponibles dépend du fichier ou du dossier particulier. En règle générale, les actions disponibles dans le menu contextuel d’un objet sont des verbes disponibles. Pour plus d’informations sur les verbes et leur disponibilité, consultez la section *verbes d’objet* du [lancement d’applications](launch.md). Pour plus d’informations sur les menus contextuels, consultez [extension des menus contextuels](context.md) . Les verbes suivants sont couramment utilisés.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**modifiés**


</dt> <dd>

Lance un éditeur et ouvre le document en vue de sa modification. Si *lpFile* n’est pas un fichier de document, la fonction échoue.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**Explorer**


</dt> <dd>

Explore le dossier spécifié par *lpFile*.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**trouver**


</dt> <dd>

Lance une recherche à partir du répertoire spécifié.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**afficher**


</dt> <dd>

Ouvre le fichier spécifié par le paramètre *lpFile* . Il peut s’agir d’un fichier exécutable, d’un fichier de document ou d’un dossier.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**étendue**


</dt> <dd>

Imprime le fichier de document spécifié par *lpFile*. Si *lpFile* n’est pas un fichier de document, la fonction échoue.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**NUL**


</dt> <dd>

Pour les systèmes antérieurs à Windows 2000, le verbe par défaut est utilisé s’il est valide et disponible dans le registre. Si ce n’est pas le cas, le verbe « Open » est utilisé.

Pour les systèmes Windows 2000 et versions ultérieures, le verbe par défaut est utilisé s’il est disponible. Si ce n’est pas le cas, le verbe « Open » est utilisé. Si aucun verbe n’est disponible, le système utilise le premier verbe listé dans le registre.

</dd> </dl> </dd> <dt>

*lpFile* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers une chaîne se terminant par un caractère **null** qui spécifie le fichier ou l’objet sur lequel exécuter le verbe spécifié. Pour spécifier un objet d’espace de noms Shell, transmettez le nom complet de l’analyse. Notez que tous les verbes ne sont pas pris en charge sur tous les objets. Par exemple, tous les types de documents ne prennent pas en charge le verbe « Print ».

</dd> <dt>

*lpParameters* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Si le paramètre *lpFile* spécifie un fichier exécutable, *lpParameters* est un pointeur vers une chaîne se terminant par un caractère **null** qui spécifie les paramètres à passer à l’application. Le format de cette chaîne est déterminé par le verbe qui doit être appelé. Si *lpFile* spécifie un fichier de document, *lpParameters* doit avoir la **valeur null**.

</dd> <dt>

*lpDirectory* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers une chaîne se terminant par un caractère **null** qui spécifie le répertoire par défaut.

</dd> <dt>

*nShowCmd* \[ dans\]
</dt> <dd>

Type : **int**

Indicateurs qui spécifient comment une application doit être affichée lorsqu’elle est ouverte. Si *lpFile* spécifie un fichier de document, l’indicateur est simplement passé à l’application associée. C’est à l’application de décider comment la gérer.

<dt>

<span id="SW_HIDE"></span><span id="sw_hide"></span>

<span id="SW_HIDE"></span><span id="sw_hide"></span>**\_masquage logiciel**


</dt> <dd>

Masque la fenêtre et active une autre fenêtre.

</dd> <dt>

<span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>

<span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>**\_optimisation logicielle**


</dt> <dd>

Agrandit la fenêtre spécifiée.

</dd> <dt>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**\_réduction logicielle**


</dt> <dd>

Réduit la fenêtre spécifiée et active la fenêtre de niveau supérieur suivante dans l’ordre de plan.

</dd> <dt>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>**\_restauration logicielle**


</dt> <dd>

Active et affiche la fenêtre. Si la fenêtre est réduite ou agrandie, Windows la restaure à sa taille et à sa position d’origine. Une application doit spécifier cet indicateur lors de la restauration d’une fenêtre réduite.

</dd> <dt>

<span id="SW_SHOW"></span><span id="sw_show"></span>

<span id="SW_SHOW"></span><span id="sw_show"></span>**\_affichage logiciel**


</dt> <dd>

Active la fenêtre et l’affiche à sa taille et à sa position actuelles.

</dd> <dt>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**\_SHOWDEFAULT SW**


</dt> <dd>

Définit l’état d’affichage basé sur l' \_ indicateur SW spécifié dans la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) transmise à la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) par le programme qui a démarré l’application. Une application doit appeler [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) avec cet indicateur pour définir l’état d’affichage initial de sa fenêtre principale.

</dd> <dt>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**\_SHOWMAXIMIZED SW**


</dt> <dd>

Active la fenêtre et l’affiche sous la forme d’une fenêtre agrandie.

</dd> <dt>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**\_SHOWMINIMIZED SW**


</dt> <dd>

Active la fenêtre et l’affiche sous forme de fenêtre réduite.

</dd> <dt>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**\_SHOWMINNOACTIVE SW**


</dt> <dd>

Affiche la fenêtre sous la forme d’une fenêtre réduite. La fenêtre active reste active.

</dd> <dt>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW \_ présenté**


</dt> <dd>

Affiche la fenêtre dans son état actuel. La fenêtre active reste active.

</dd> <dt>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**\_SHOWNOACTIVATE SW**


</dt> <dd>

Affiche une fenêtre à sa taille et à sa position les plus récentes. La fenêtre active reste active.

</dd> <dt>

<span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>

<span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>**\_SHOWNORMAL SW**


</dt> <dd>

Active et affiche une fenêtre. Si la fenêtre est réduite ou agrandie, Windows la restaure à sa taille et à sa position d’origine. Une application doit spécifier cet indicateur lors de l’affichage de la fenêtre pour la première fois.

</dd> </dl> </dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Type : **void \** _

Fonction de rappel utilisée pour appeler [_ *CreateProcess* *](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) dans le noyau 16 bits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HINSTANCE**

Retourne une valeur supérieure à 32 en cas de réussite, ou une valeur d’erreur inférieure ou égale à 32 dans le cas contraire. Le tableau suivant répertorie les valeurs d’erreur. La valeur de retour est castée en tant que HINSTANCE pour la compatibilité descendante avec les applications Windows 16 bits. Toutefois, ce n’est pas un véritable HINSTANCE. La seule chose qui peut être effectuée avec le HINSTANCE retourné est de le convertir en **int** et de le comparer à la valeur 32 ou à l’un des codes d’erreur ci-dessous.



| Code de retour                                                                                             | Description                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | Le système d’exploitation ne dispose pas de suffisamment de mémoire ou de ressources.<br/>                                                                                                           |
| <dl> <dt>**\_fichier d' \_ erreur \_ introuvable**</dt> </dl>  | Le fichier spécifié est introuvable.<br/>                                                                                                                             |
| <dl> <dt>**\_chemin d' \_ erreur \_ introuvable**</dt> </dl>  | Le chemin spécifié est introuvable.<br/>                                                                                                                             |
| <dl> <dt>**\_format incorrect de l’erreur \_**</dt> </dl>       | Le fichier. exe n’est pas valide (non Win32. exe ou erreur dans l’image. exe).<br/>                                                                                             |
| <dl> <dt>**SE \_ ACCESSDENIED d’erreur \_**</dt> </dl>    | Le système d’exploitation a refusé l’accès au fichier spécifié.<br/>                                                                                                     |
| <dl> <dt>**SE \_ ASSOCINCOMPLETE d’erreur \_**</dt> </dl> | L’Association du nom de fichier est incomplète ou non valide.<br/>                                                                                                           |
| <dl> <dt>**SE \_ DDEBUSY d’erreur \_**</dt> </dl>         | La transaction DDE n’a pas pu être effectuée, car d’autres transactions DDE étaient en cours de traitement.<br/>                                                               |
| <dl> <dt>**SE \_ DDEFAIL d’erreur \_**</dt> </dl>         | Échec de la transaction DDE.<br/>                                                                                                                                   |
| <dl> <dt>**SE \_ DDETIMEOUT d’erreur \_**</dt> </dl>      | La transaction DDE n’a pas pu aboutir car la demande a expiré.<br/>                                                                                     |
| <dl> <dt>**SE \_ DLLNOTFOUND d’erreur \_**</dt> </dl>     | La DLL spécifiée est introuvable.<br/>                                                                                                                              |
| <dl> <dt>**erreur SE- \_ \_ FNF**</dt> </dl>             | Le fichier spécifié est introuvable.<br/>                                                                                                                             |
| <dl> <dt>**SE \_ Err \_ noassoc**</dt> </dl>         | Aucune application n’est associée à l’extension de nom de fichier donnée. Cette erreur est également retournée si vous tentez d’imprimer un fichier qui n’est pas imprimable.<br/> |
| <dl> <dt>**SE \_ insuffisance d’erreur \_**</dt> </dl>             | La mémoire est insuffisante pour terminer l’opération.<br/>                                                                                                        |
| <dl> <dt>**SE \_ Err. \_ PNF**</dt> </dl>             | Le chemin spécifié est introuvable.<br/>                                                                                                                             |
| <dl> <dt>**\_partage d’Err. se \_**</dt> </dl>           | Une violation de partage s’est produite.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Notes

**WOWShellExecute** n’est pas inclus dans un en-tête ou un fichier. lib. Elle est exportée à partir de Shell32.dll par son nom.

Cette méthode vous permet d’exécuter des commandes dans le menu contextuel d’un dossier ou stockées dans le registre.

Si *lpOperation* a la **valeur null**, la fonction ouvre le fichier spécifié par *lpFile*. Si *lpOperation* est « Open » ou « explore », la fonction tente d’ouvrir ou d’explorer le dossier.

Pour obtenir des informations sur l’application qui est lancée suite à l’appel de **WOWShellExecute**, utilisez [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> Le paramètre **Démarrer le dossier Windows dans un processus distinct** dans les options des dossiers affecte **WOWShellExecute**. Si cette option est désactivée (paramètre par défaut), **WOWShellExecute** utilise une fenêtre d’Explorateur ouverte au lieu d’en lancer une nouvelle. Si aucune fenêtre d’explorateur n’est ouverte, **WOWShellExecute** en lance une nouvelle.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
