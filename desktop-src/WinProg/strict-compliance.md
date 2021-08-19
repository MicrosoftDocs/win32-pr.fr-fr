---
title: Conformité STRICTe
description: Un code source qui se compile correctement peut générer des messages d’erreur lorsque vous activez la vérification de type STRICTe.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29baee071bd8d7c236ec5f2f99d1dff11aeac37deb44b0d8a6254325c9a75df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928144"
---
# <a name="strict-compliance"></a>Conformité STRICTe

Un code source qui se compile correctement peut générer des messages d’erreur lorsque vous activez la vérification de type **stricte** . Les sections suivantes décrivent la configuration minimale requise pour la compilation de votre code lorsque **strict** est activé. Des étapes supplémentaires sont recommandées, en particulier pour produire du code portable.

## <a name="general-requirements"></a>Exigences générales

La principale exigence est que vous devez déclarer des types de handle et des pointeurs de fonction corrects au lieu de vous appuyer sur des types plus généraux. Vous ne pouvez pas utiliser un type de handle dans lequel un autre est attendu. Cela signifie également que vous devrez peut-être modifier les déclarations de fonction et utiliser d’autres casts de type.

Pour de meilleurs résultats, le type de **handle** générique doit être utilisé uniquement lorsque cela est nécessaire.

## <a name="declaring-functions-within-your-application"></a>Déclaration de fonctions dans votre application

Assurez-vous que toutes les fonctions d’application sont déclarées. Il est recommandé de placer toutes les déclarations de fonction dans un fichier include, car vous pouvez facilement analyser vos déclarations et rechercher les types de paramètres et de retour qui doivent être modifiés.

Si vous utilisez l’option de compilateur **/ZG** pour créer des fichiers d’en-tête pour vos fonctions, n’oubliez pas que vous obtiendrez des résultats différents selon que vous avez activé la vérification de type **stricte** . Si la fonction **strict** est désactivée, tous les types de handles génèrent le même type de base. Si l’option **strict** est activée, elles génèrent des types de base différents. Pour éviter les conflits, vous devez recréer le fichier d’en-tête chaque fois que vous activez ou désactivez **strict**, ou modifiez le fichier d’en-tête pour utiliser les types **HWND**, **HDC**, **handle**, etc., au lieu des types de base.

toutes les déclarations de fonction que vous avez copiées à partir de Windows. h dans votre code source ont peut-être changé et votre déclaration locale peut être obsolète. Supprimez votre déclaration locale.

## <a name="types-that-require-casts"></a>Types qui requièrent des casts

Certaines fonctions ont des paramètres ou des types de retour génériques. Par exemple, la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) retourne des données qui peuvent être de n’importe quel nombre de types, en fonction du contexte. Lorsque vous voyez l’une de ces fonctions dans votre code source, assurez-vous que vous utilisez la conversion de type correcte et qu’elle est la plus spécifique possible. La liste suivante est un exemple de ces fonctions.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Quand vous appelez [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)ou [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), vous devez d’abord convertir le résultat en type **uint \_ ptr**. Vous devez effectuer des étapes similaires pour toute fonction qui retourne une valeur **LRESULT** ou **long \_ ptr** , où le résultat contient un descripteur. Cela est nécessaire pour écrire du code portable, car la taille d’une poignée varie selon la version de Windows. Le cast (**uint \_ ptr**) garantit une conversion correcte. Le code suivant montre un exemple dans lequel **SendMessage** retourne un handle à un pinceau :


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



Les paramètres **CreateWindow** et **CreateWindowEx** *HMENU* sont parfois utilisés pour passer un identificateur de contrôle entier (ID). Dans ce cas, vous devez effectuer un cast de l’ID en un type **HMENU** :


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a>Considérations supplémentaires

Pour tirer le meilleur parti de la vérification de type **stricte** , vous devez suivre des instructions supplémentaires. votre code sera plus portable dans les futures versions de Windows si vous apportez les modifications suivantes.

Les types **wParam**, **lParam**, **LRESULT** et **LPVOID** sont des *types de données polymorphes*. Ils contiennent différents genres de données à des moments différents, même si la vérification de type **stricte** est activée. Pour tirer parti de la vérification de type, vous devez effectuer un cast des valeurs de ces types dès que possible. (Notez que les craqueurs de messages refont automatiquement *wParam* et *lParam* pour vous de manière portable.)

Faites particulièrement attention pour distinguer les types **HMODULE** et **HINSTANCE** . Même si **strict** est activé, ils sont définis comme étant du même type de base. La plupart des fonctions de gestion du module de noyau utilisent des types **HINSTANCE** , mais il existe quelques fonctions qui retournent ou acceptent uniquement des types **HMODULE** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Désactivation de STRICT](disabling-strict.md)
</dt> <dt>

[Activation du STRICT](enabling-strict.md)
</dt> </dl>

 

 