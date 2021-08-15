---
description: Les objets d’interface utilisateur ne prennent en charge qu’un seul handle par objet. Les processus ne peuvent pas hériter ou dupliquer des handles d’objets utilisateur. Les processus d’une session ne peuvent pas faire référence à un handle d’utilisateur dans une autre session.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Objets utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c3cdb5c0927a5773bad818064442f654159fefba2b2dfa4d0cb4c08d17ff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884322"
---
# <a name="user-objects"></a>Objets utilisateur

Les objets d’interface utilisateur ne prennent en charge qu’un seul handle par objet. Les processus ne peuvent pas hériter ou dupliquer des handles d’objets utilisateur. Les processus d’une session ne peuvent pas faire référence à un handle d’utilisateur dans une autre session.

Il existe une limite théorique de 65 536 descripteurs utilisateur par session. Toutefois, le nombre maximal de descripteurs utilisateur qui peuvent être ouverts par session est généralement plus faible, car il est affecté par la mémoire disponible. Il y a également une limite par processus par défaut des handles utilisateur. Pour modifier cette limite, définissez la valeur de Registre suivante :

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Cette valeur peut être définie sur un nombre compris entre 200 et 18 000.

## <a name="handles-to-user-objects"></a>Handles vers des objets utilisateur

Les handles vers les objets utilisateur sont publics pour tous les processus. Autrement dit, tout processus peut utiliser le handle d’objet utilisateur, à condition que le processus ait un accès de sécurité à l’objet.

Dans l’illustration suivante, une application crée un objet Window. La fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) crée l’objet de fenêtre et retourne un handle d’objet.

![application créant un objet Window](images/cshob-01.png)

Une fois l’objet Window créé, l’application peut utiliser le handle de fenêtre pour afficher ou modifier la fenêtre. Le descripteur reste valide jusqu’à ce que l’objet Window soit détruit.

Dans l’illustration suivante, l’application détruit l’objet Window. La fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) supprime l’objet Window de la mémoire, ce qui invalide le handle de fenêtre.

![destruction d’un objet Window](images/cshob-02.png)

## <a name="managing-user-objects"></a>Gestion des objets utilisateur

Le tableau suivant répertorie les objets utilisateur, ainsi que les fonctions de création et de destruction de chaque objet. Les fonctions Creator créent l’objet et un handle d’objet, ou simplement retournent simplement le handle d’objet existant. Les fonctions Destroy suppriment l’objet de la mémoire, ce qui invalide le descripteur d’objet.



| Objet utilisateur       | Creator, fonction                                                                                                                                                                                                                                                              | Fonction Destroy                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Table d’accélérateurs | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Signe insertion             | [**CreateCaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Curseur            | [**CreateCursor**](/windows/win32/api/winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Conversation DDE  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Hook              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Icône              | [**CreateIconIndirect**](/windows/win32/api/winuser/nf-winuser-createiconindirect), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menu              | [**CreateMenu**](/windows/win32/api/winuser/nf-winuser-createmenu), [**CreatePopupMenu**](/windows/win32/api/winuser/nf-winuser-createpopupmenu), [**LoadMenu**](/windows/win32/api/winuser/nf-winuser-loadmenua), [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Fenêtre            | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**CreateDialogParam**](/windows/win32/api/winuser/nf-winuser-createdialogparama), [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama), [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Position de la fenêtre   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
