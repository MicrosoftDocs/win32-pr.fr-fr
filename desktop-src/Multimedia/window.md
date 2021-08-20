---
title: fenêtre (commande)
description: La commande de fenêtre contrôle la fenêtre d’affichage.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- commande windows Windows multimédia
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c65fe13309d30a3aff94e6e78dc0ab1fbcfec26aa1634e8dae72130370cc8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800703"
---
# <a name="window-command"></a>fenêtre (commande)

La commande de fenêtre contrôle la fenêtre d’affichage. Vous pouvez utiliser cette commande pour modifier les caractéristiques d’affichage de la fenêtre ou fournir une fenêtre de destination que le pilote utilisera à la place de la fenêtre d’affichage par défaut. Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("window %s %s %s"), 
  lpszDeviceID, 
  lpszWindowFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

Indicateur de contrôle de la fenêtre d’affichage. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande de fenêtre et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                                                                                                        | Signification                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | gérer l’état *HWND* hidestate minimizestate restorestate showshow agrandi                                                                    | afficher minimizedshow [**min**](min.md) noactiveshow nashow *noactivateshow NormalText*                                             |
| superposition      | fixedhandle defaulthandle *maximizedstate* État hidestate iconicstate minimizestate minimizedstate ActionState aucun noactivatestate normal | State restorestate showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *Caption* |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszWindowFlags** et leurs significations.



| Valeur                            | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixe                            | Désactive l’étirement de l’image.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| gérer les valeurs par défaut                   | Spécifie que l’appareil doit rétablir la fenêtre d’affichage par défaut créée pendant l’opération d' [ouverture](open.md) . Pour les périphériques de superposition vidéo, spécifie que l’appareil doit créer et gérer sa propre fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                  |
| handle *HWND*                    | Spécifie le handle de la fenêtre de destination à utiliser à la place de la fenêtre par défaut. Le paramètre *HWND* contient l’équivalent numérique ASCII du handle de fenêtre retourné par la fonction [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Deux instances d’appareil peuvent utiliser le même handle de fenêtre, à condition que chaque instance met à jour les pixels de la vidéo et de l’image dans la fenêtre comme si l’autre instance n’existait pas. Quand la sortie vidéo est désactivée avec [setvideo](setvideo.md) « OFF », une commande de [mise à jour](update.md) rend le rectangle de destination une couleur unie. |
| afficher les agrandissements                   | Agrandit la fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| afficher [**min**](min.md) NoActive | Affiche la fenêtre de destination sous la forme d’une icône.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| afficher les fenêtres réduites                   | Réduit la fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| afficher na                          | Affiche la fenêtre de destination dans son état actuel. la fenêtre actuellement active reste active.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| afficher noactivate                  | Affiche la fenêtre de destination dans sa taille et sa position les plus récentes. la fenêtre actuellement active reste active.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| afficher normal                      | Active et affiche la fenêtre de destination à sa taille et à sa position d’origine. (Il s’agit de la même chose que l’indicateur « State Restore ».)                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| masquer l’État                       | Masque la fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| sous forme d’État                     | Affiche la fenêtre de destination sous la forme d’une icône.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| État agrandi                  | Agrandit la fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| réduction de l’État                   | Réduit la fenêtre de destination et active la fenêtre de niveau supérieur dans la liste du gestionnaire de fenêtres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| État réduit                  | Réduit la fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| État-aucune action                  | Affiche la fenêtre de destination dans son état actuel. La fenêtre actuellement active reste active.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| État noactivate                 | Affiche la fenêtre de destination dans sa taille et son état les plus récents. La fenêtre actuellement active reste active.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| état normal                     | Active et affiche la fenêtre de destination à sa taille et à sa position d’origine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| restauration de l’État                    | Active et affiche la fenêtre de destination à sa taille et à sa position d’origine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| affichage de l’État                       | Affiche la fenêtre de destination.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| étirement                          | Active l’étirement de l’image.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| *légende* de texte                   | Spécifie la légende de la fenêtre de destination. Si ce texte contient des espaces incorporés, la légende entière doit être placée entre guillemets. La légende par défaut de la fenêtre par défaut est vide.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les périphériques de superposition vidéo créent et affichent généralement une fenêtre lorsqu’ils sont ouverts. Si votre application fournit une fenêtre au pilote, votre application est responsable de la gestion des messages envoyés à la fenêtre.

Étant donné que vous pouvez utiliser la commande [Status](status.md) pour récupérer le handle de la fenêtre d’affichage du pilote, vous pouvez également utiliser les fonctions du gestionnaire de fenêtres standard (telles que [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) pour manipuler la fenêtre.

## <a name="examples"></a>Exemples

La commande suivante affiche et définit la légende de la fenêtre de lecture du « film ».

``` syntax
window movie text "Welcome to the Movies" state show
```

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[répétition](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

