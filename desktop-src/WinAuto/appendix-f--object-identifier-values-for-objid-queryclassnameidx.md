---
title: Annexe F valeurs de l’identificateur d’objet pour OBJID_QUERYCLASSNAMEIDX
description: Lorsque OLEACC envoie un \_ message WM GETOBJECT avec le paramètre lParam défini sur OBJIDQUERYCLASSNAMEIDX, un grand nombre d’utilisateurs standard ou de contrôles communs (COMCTL) retournent l’une des valeurs suivantes.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22368f15fa40e30f909f9ad838cb478ed1e9a9c9ff25929f63bb91ec99e99b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134032"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Annexe F : valeurs de l’identificateur d’objet pour OBJID \_ QUERYCLASSNAMEIDX

Lorsque OLEACC envoie un message [**WM \_ GETOBJECT**](wm-getobject.md) avec le paramètre *lParam* défini sur OBJIDQUERYCLASSNAMEIDX, un grand nombre d’utilisateurs standard ou de contrôles communs (COMCTL) retournent l’une des valeurs suivantes.



| UTILISATEUR ou contrôle commun | Valeur retournée |
|------------------------|--------------|
| ListBox                | 65536 + 0      |
| Bouton                 | 65536 + 2      |
| statique                 | 65536 + 3      |
| Modifier                   | 65536 + 4      |
| Combobox               | 65536 + 5      |
| Scrollbar              | 65536 + 10     |
| Statut                 | 65536 + 11     |
| Barre d’outils                | 65536 + 12     |
| Avancement               | 65536 + 13     |
| Immobile                | 65536 + 14     |
| Onglet                    | 65536 + 15     |
| Touche d’accès rapide                 | 65536 + 16     |
| En-tête                 | 65536 + 17     |
| TrackBar               | 65536 + 18     |
| Liste               | 65536 + 19     |
| UpDown                 | 65536 + 22     |
| Info-bulles               | 65536 + 24     |
| TreeView               | 65536 + 25     |
| RichEdit               | 65536 + 28     |



 

seuls les contrôles communs USER et Windows (COMCTL) retournent l’une des valeurs de la table. Si une fenêtre retourne 0 en réponse à ce message, la fenêtre peut être l’une des suivantes :

-   Un contrôle personnalisé
-   Contrôle autre que l’un des contrôles du tableau précédent
-   Une ancienne version d’un contrôle système qui ne reconnaît pas le message [**WM de \_ GETOBJECT**](wm-getobject.md)

Si une fenêtre retourne la valeur 0, les clients devront peut-être utiliser [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) ou [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname). Vous pouvez utiliser ces fonctions pour déterminer le type de contrôle en fonction du nom de la classe.

En général, les clients peuvent utiliser les informations fournies par OLEACC.

 

 