---
description: Démarre l’aide de Windows (Winhelp.exe) et transmet des données supplémentaires qui indiquent la nature de l’aide demandée par l’application.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: MLWinHelp fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLWinHelp
- MLWinHelpA
- MLWinHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: badfeb599fd24fd255eb064bbaf6d99a3b758bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972315"
---
# <a name="mlwinhelp-function"></a>MLWinHelp fonction)

\[Cette fonction est disponible via Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Démarre l’aide de Windows (Winhelp.exe) et transmet des données supplémentaires qui indiquent la nature de l’aide demandée par l’application.

## <a name="syntax"></a>Syntaxe


```C++
BOOL MLWinHelp(
  _In_ HWND      hWndMain,
  _In_ LPCTSTR   lpszHelp,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hWndMain* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre qui demande de l’aide. La fonction **MLWinHelp** utilise ce handle pour assurer le suivi des applications qui ont demandé de l’aide. Si le paramètre *uCommand* spécifie Help \_ CONTEXTMENU ou Help \_ WM \_ , *hWndMain* identifie le contrôle qui demande de l’aide.

</dd> <dt>

*lpszHelp* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Adresse d’une chaîne terminée par le caractère null qui contient le chemin d’accès, si nécessaire, et le nom du fichier d’aide que **MLWinHelp** doit afficher.

Le nom de fichier peut être suivi d’un chevron (>) et du nom d’une fenêtre secondaire si la rubrique doit être affichée dans une fenêtre secondaire plutôt que dans la fenêtre principale. Vous devez définir le nom de la fenêtre secondaire dans la \[ \] section Windows du fichier du projet d’aide (. hpj).

</dd> <dt>

*uCommand* \[ dans\]
</dt> <dd>

Type : **uint**

Type d’aide demandé. Pour obtenir la liste des valeurs possibles et la manière dont elles affectent la valeur à placer dans le paramètre *dwData* , consultez la section Notes.

</dd> <dt>

*dwData* \[ dans\]
</dt> <dd>

Type : **\_ ptr DWORD**

Données supplémentaires. La valeur utilisée dépend de la valeur du paramètre *uCommand* . Pour obtenir la liste des valeurs *dwData* possibles, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Cette fonction n’est pas incluse dans un fichier d’en-tête et doit être appelée par le numéro ordinal 395 pour **MLWinHelpA** et 397 pour **MLWinHelpW**.

**MLWinHelp** est essentiellement un wrapper pour [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Il tente d’obtenir le chemin d’accès au fichier d’aide correspondant au paramètre de langue de l’interface utilisateur actuel avant d’appeler **WinHelp**. Si elle réussit, elle passe ce chemin d’accès. En cas d’échec, il passe le chemin d’accès pointé par *lpszHelp*.

Cette fonction échoue si elle est appelée à partir de n’importe quel contexte mais de l’utilisateur actuel.

Avant de fermer la fenêtre qui a demandé de l’aide, l’application doit appeler **MLWinHelp** avec le paramètre *UCOMMAND* défini pour aider à \_ quitter. Tant que toutes les applications n’ont pas effectué cette opération, l’aide de Windows ne se termine pas. Notez qu’il n’est pas nécessaire d’appeler l’aide de Windows avec la \_ commande aide Quit si vous avez utilisé la \_ commande help CONTEXTPOPUP pour démarrer l’aide de Windows.

Le tableau suivant indique les valeurs possibles pour le paramètre *uCommand* et les formats correspondants du paramètre *dwData* .



| *uCommand*          | Action                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AIDE ( \_ commande)       | Exécute une macro d’aide ou une chaîne de macro.                                                                                                                                                                                                                               | Adresse d’une chaîne qui spécifie le nom de la ou des macros d’aide à exécuter. Si la chaîne spécifie plusieurs noms de macro, ceux-ci doivent être séparés par des points-virgules. Vous devez utiliser la forme abrégée du nom de macro pour certaines macros, car l’aide de Windows ne prend pas en charge le nom long.                         |
| Sommaire de l’aide \_      | Affiche la rubrique spécifiée par l’option Sommaire de la \[ \] section Options du fichier. hpj. Cette commande est destinée à la compatibilité descendante. Les nouvelles applications doivent fournir un fichier. CNT et utiliser la commande de recherche de l’aide \_ .                                           | Pas défini sur 0.                                                                                                                                                                                                                                                                                           |
| contexte d’aide \_       | Affiche la rubrique identifiée par l’identificateur de contexte spécifié défini dans \[ la \] section Map du fichier. hpj.                                                                                                                                                   | Contient l’identificateur de contexte pour la rubrique.                                                                                                                                                                                                                                                               |
| HELP \_ CONTEXTMENU   | Affiche le menu **aide** pour la fenêtre sélectionnée, puis affiche la rubrique du contrôle sélectionné dans une fenêtre indépendante.                                                                                                                                             | Adresse d’un tableau de paires **DWORD** . Le premier **DWORD** de chaque paire est l’identificateur de contrôle, tandis que le second est l’identificateur de contexte de la rubrique. Le tableau doit se terminer par une paire de zéros {0,0} . Si vous ne souhaitez pas ajouter d’aide à un contrôle particulier, affectez la valeur-1 à son identificateur de contexte. |
| AIDE \_ CONTEXTPOPUP  | Affiche la rubrique identifiée par l’identificateur de contexte spécifié défini dans \[ la \] section Map du fichier. hpj dans une fenêtre indépendante.                                                                                                                                | Contient l’identificateur de contexte pour une rubrique.                                                                                                                                                                                                                                                                 |
| recherche d’aide \_        | Affiche la boîte de dialogue **rubriques d’aide** .                                                                                                                                                                                                                             | Pas défini sur 0.                                                                                                                                                                                                                                                                                           |
| AIDE \_ FORCEFILE     | Garantit que l’aide de Windows affiche le fichier d’aide correct. Si le fichier d’aide incorrect est affiché, l’aide de Windows ouvre la bonne. Sinon, il n’y a aucune action.                                                                                     | Pas défini sur 0.                                                                                                                                                                                                                                                                                           |
| AIDE \_ HELPONHELP    | Affiche de l’aide sur l’utilisation de l’aide de Windows, si le fichier WinHlp32. hlp est disponible.                                                                                                                                                                                     | Pas défini sur 0.                                                                                                                                                                                                                                                                                           |
| INDEX de l’aide \_         | Affiche la rubrique spécifiée par l’option Sommaire de la \[ \] section Options du fichier. hpj. Cette commande est destinée à la compatibilité descendante. Les nouvelles applications doivent utiliser la commande de recherche de l’aide \_ .                                                                   | Pas défini sur 0.                                                                                                                                                                                                                                                                                           |
| \_touche aide           | Affiche la rubrique dans le tableau de mots clés qui correspond au mot clé spécifié, s’il existe une correspondance exacte. S’il existe plusieurs correspondances, affiche l’index avec les rubriques répertoriées dans la zone de liste **rubriques trouvées** .                                                 | Adresse d’une chaîne de mot clé. Plusieurs mots clés doivent être séparés par des points-virgules.                                                                                                                                                                                                                              |
| AIDE \_ relations      | Affiche la rubrique spécifiée par un mot clé dans une autre table de mots clés.                                                                                                                                                                                           | Adresse d’une structure [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) qui spécifie un caractère de note de bas de page de table et un mot clé.                                                                                                                                                                                     |
| AIDE \_ PARTIALKEY    | Affiche la rubrique dans le tableau de mots clés qui correspond au mot clé spécifié, s’il existe une correspondance exacte. S’il existe plusieurs correspondances, affiche la boîte de dialogue **rubriques trouvées** . Pour afficher l’index sans passer un mot clé, utilisez un pointeur vers une chaîne vide. | Adresse d’une chaîne de mot clé. Plusieurs mots clés doivent être séparés par des points-virgules.                                                                                                                                                                                                                              |
| AIDE \_ quitter          | Informe l’aide de Windows qu’elle n’est plus nécessaire. Si aucune autre application n’a demandé de l’aide, Windows ferme l’aide Windows.                                                                                                                                         | Pas défini sur 0.                                                                                                                                                                                                                                                                                           |
| AIDE \_ SETCONTENTS   | Spécifie la rubrique relative au contenu. L’aide de Windows affiche cette rubrique lorsque l’utilisateur clique sur le bouton **Sommaire** si aucun fichier. CNT n’est associé au fichier d’aide.                                                                                                  | Contient l’identificateur de contexte pour la rubrique du contenu.                                                                                                                                                                                                                                                      |
| AIDE \_ SETPOPUP \_ pos | Définit la position de la fenêtre contextuelle suivante.                                                                                                                                                                                                                   | Contient les données de position. Utilisez la macro [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) pour concaténer les coordonnées horizontales et verticales en une seule valeur. La fenêtre contextuelle est positionnée comme si le curseur de la souris était au point spécifié lors de l’appel de la fenêtre contextuelle.                                 |
| AIDE \_ SETWINPOS     | Affiche la fenêtre d’aide Windows, si elle est réduite ou en mémoire, et définit sa taille et sa position comme spécifié.                                                                                                                                                      | Adresse d’une structure [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) qui spécifie la taille et la position d’une fenêtre d’aide principale ou secondaire.                                                                                                                                                             |
| AIDE \_ TCARD         | Indique qu’une commande est destinée à une instance de carte de formation de l’aide de Windows. Combinez cette commande avec d’autres commandes à l’aide de l’opérateur or au niveau du bit.                                                                                                                    | Dépend de la commande avec laquelle cette commande est combinée.                                                                                                                                                                                                                                                  |
| aide \_ WM \_      | Affiche la rubrique pour le contrôle identifié par le paramètre *hWndMain* dans une fenêtre indépendante.                                                                                                                                                                        | Adresse d’un tableau de paires **DWORD** . Le premier **DWORD** de chaque paire est un identificateur de contrôle, et le deuxième est un identificateur de contexte pour une rubrique. Le tableau doit se terminer par une paire de zéros {0,0} . Si vous ne souhaitez pas ajouter d’aide à un contrôle particulier, affectez la valeur-1 à son identificateur de contexte.       |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **MLWinHelpW** (Unicode) et **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
