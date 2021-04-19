---
description: Chaque fenêtre est un membre d’une classe de fenêtre particulière. La classe de fenêtre détermine la procédure de fenêtre par défaut utilisée par une fenêtre individuelle pour traiter ses messages.
ms.assetid: 3a8e8f4e-910d-4863-a4a7-dd37c2dfa402
title: À propos des procédures de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f63586b9ca4ac6fe8486ba112316174533b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522450"
---
# <a name="about-window-procedures"></a>À propos des procédures de fenêtre

Chaque fenêtre est un membre d’une classe de fenêtre particulière. La classe de fenêtre détermine la procédure de fenêtre par défaut utilisée par une fenêtre individuelle pour traiter ses messages. Toutes les fenêtres appartenant à la même classe utilisent la même procédure de fenêtre par défaut. Par exemple, le système définit une procédure de fenêtre pour la classe de zone de liste déroulante (**ComboBox**); toutes les zones de liste déroulante utilisent ensuite cette procédure de fenêtre.

Une application inscrit généralement au moins une nouvelle classe de fenêtre et la procédure de fenêtre qui lui est associée. Après l’inscription d’une classe, l’application peut créer de nombreuses fenêtres de cette classe, qui utilisent toutes la même procédure de fenêtre. Comme cela signifie que plusieurs sources peuvent appeler simultanément le même morceau de code, vous devez faire attention lorsque vous modifiez des ressources partagées à partir d’une procédure de fenêtre. Pour plus d’informations, consultez [classes de fenêtre](window-classes.md).

Les procédures de fenêtre pour les boîtes de dialogue (appelées procédures de boîte de dialogue) ont une structure et une fonction similaires à celles des procédures de fenêtre normales. Tous les points faisant référence aux procédures de fenêtre dans cette section s’appliquent également aux procédures de boîte de dialogue. Pour plus d’informations, consultez [boîtes de dialogue](/windows/desktop/dlgbox/dialog-boxes).

Cette section décrit les rubriques suivantes.

-   [Structure d’une procédure de fenêtre](#structure-of-a-window-procedure)
-   [Procédure de fenêtre par défaut](#default-window-procedure)
-   [Sous-classe de procédure de fenêtre](#window-procedure-subclassing)
    -   [Sous-classe d’instance](#instance-subclassing)
    -   [Sous-classement global](#global-subclassing)
-   [Superclassement de la procédure de fenêtre](#window-procedure-superclassing)

## <a name="structure-of-a-window-procedure"></a>Structure d’une procédure de fenêtre

Une procédure de fenêtre est une fonction qui a quatre paramètres et retourne une valeur signée. Les paramètres se composent d’un handle de fenêtre, d’un identificateur de message **uint** et de deux paramètres de message déclarés avec les types de données **wParam** et **lParam** . Pour plus d’informations, consultez [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).

Les paramètres de message contiennent souvent des informations à la fois dans leurs mots de poids faible et de poids fort. Une application peut utiliser plusieurs macros pour extraire des informations à partir des paramètres de message. La macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) , par exemple, extrait le mot de poids faible (bits de 0 à 15) à partir d’un paramètre de message. Les autres macros incluent [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))et [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)).

L’interprétation de la valeur de retour dépend du message en question. Consultez la description de chaque message pour déterminer la valeur de retour appropriée.

Étant donné qu’il est possible d’appeler une procédure de fenêtre de manière récursive, il est important de réduire le nombre de variables locales qu’il utilise. Lors du traitement de messages individuels, une application doit appeler des fonctions en dehors de la procédure de fenêtre pour éviter une utilisation excessive des variables locales, ce qui peut provoquer un dépassement de capacité de la pile pendant une récurrence profonde.

## <a name="default-window-procedure"></a>Procédure de fenêtre par défaut

La fonction de la procédure de fenêtre par défaut, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) définit certains comportements fondamentaux partagés par toutes les fenêtres. La procédure de fenêtre par défaut fournit les fonctionnalités minimales pour une fenêtre. Une procédure de fenêtre définie par l’application doit passer tous les messages qu’elle ne traite pas à la fonction **DefWindowProc** pour le traitement par défaut.

## <a name="window-procedure-subclassing"></a>Sous-classe de procédure de fenêtre

Quand une application crée une fenêtre, le système alloue un bloc de mémoire pour stocker des informations spécifiques à la fenêtre, y compris l’adresse de la procédure de fenêtre qui traite les messages pour la fenêtre. Lorsque le système doit transmettre un message à la fenêtre, il recherche les informations spécifiques à la fenêtre pour l’adresse de la procédure de fenêtre et transmet le message à cette procédure.

Le *sous-classing* est une technique qui permet à une application d’intercepter et de traiter les messages envoyés ou publiés dans une fenêtre particulière avant que la fenêtre n’ait la possibilité de les traiter. En sous-classant une fenêtre, une application peut augmenter, modifier ou surveiller le comportement de la fenêtre. Une application peut sous-classe une fenêtre appartenant à une classe globale système, telle qu’un contrôle d’édition ou une zone de liste. Par exemple, une application peut sous-définir un contrôle d’édition pour empêcher le contrôle d’accepter certains caractères. Toutefois, vous ne pouvez pas sous-classe une fenêtre ou une classe qui appartient à une autre application. Toutes les sous-classes doivent être exécutées dans le même processus.

Une application sous-classe une fenêtre en remplaçant l’adresse de la procédure de fenêtre d’origine de la fenêtre par l’adresse d’une nouvelle procédure de fenêtre, appelée *procédure de sous-classe*. Par la suite, la procédure de sous-classe reçoit tous les messages envoyés ou publiés dans la fenêtre.

La procédure de sous-classe peut effectuer trois actions lors de la réception d’un message : elle peut passer le message à la procédure de fenêtre d’origine, modifier le message et le passer à la procédure de fenêtre d’origine, ou traiter le message et ne pas le passer à la procédure de fenêtre d’origine. Si la procédure de sous-classe traite un message, elle peut le faire avant, après ou avant et après la transmission du message à la procédure de fenêtre d’origine.

Le système fournit deux types de sous-classes : [instance](#instance-subclassing) et [Global](#global-subclassing). Dans le sous-processus d' *instance*, une application remplace l’adresse de la procédure de fenêtre d’une seule instance d’une fenêtre. Une application doit utiliser la sous-classe d’instance pour la sous-classe d’une fenêtre existante. Dans le sous-modèle *Global*, une application remplace l’adresse de la procédure de fenêtre dans la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) d’une classe de fenêtre. Toutes les fenêtres suivantes créées avec la classe ont l’adresse de la procédure de sous-classe, mais les fenêtres existantes de la classe ne sont pas affectées.

### <a name="instance-subclassing"></a>Sous-classe d’instance

Une application sous-classe une instance d’une fenêtre à l’aide de la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . L’application transmet l' **indicateur \_ WNDPROC GWL** , le handle de la fenêtre à la sous-classe et l’adresse de la procédure de sous-classe à **SetWindowLong**. La procédure de sous-classe peut résider dans l’exécutable de l’application ou dans une DLL.

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) retourne l’adresse de la procédure de fenêtre d’origine de la fenêtre. L’application doit enregistrer l’adresse, en l’utilisant dans les appels suivants à la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) , pour transmettre les messages interceptés à la procédure de fenêtre d’origine. L’application doit également avoir l’adresse de la procédure de fenêtre d’origine pour supprimer la sous-classe de la fenêtre. Pour supprimer la sous-classe, l’application appelle à nouveau **SetWindowLong** , en passant l’adresse de la procédure de fenêtre d’origine avec l’indicateur **\_ WNDPROC GWL** et le handle à la fenêtre.

Le système est propriétaire des classes globales du système et les aspects des contrôles peuvent passer d’une version du système à l’autre. Si l’application doit sous-classe une fenêtre qui appartient à une classe globale système, le développeur peut avoir besoin de mettre à jour l’application lorsqu’une nouvelle version du système est publiée.

Dans la mesure où la sous-classe d’instance se produit après la création d’une fenêtre, vous ne pouvez pas ajouter d’octets supplémentaires à la fenêtre. Les applications qui sous-classent une fenêtre doivent utiliser la liste de propriétés de la fenêtre pour stocker toutes les données nécessaires pour une instance de la fenêtre sous-classée. Pour plus d’informations, consultez Propriétés de la [fenêtre](window-properties.md).

Lorsqu’une application sous-classe une fenêtre sous-classée, elle doit supprimer les sous-classes dans l’ordre inverse dans lequel elles ont été exécutées. Si l’ordre de suppression n’est pas inversé, une erreur système irrécupérable peut se produire.

### <a name="global-subclassing"></a>Sous-classement global

Pour une sous-classe globale d’une classe de fenêtre, l’application doit avoir un handle vers une fenêtre de la classe. L’application a également besoin du handle pour supprimer la sous-classe. Pour obtenir le descripteur, une application crée généralement une fenêtre masquée de la classe à sous-classée. Une fois le descripteur obtenu, l’application appelle la fonction [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , en spécifiant le descripteur, l’indicateur **\_ WNDPROC GCL** et l’adresse de la procédure de sous-classe. **SetClassLong** retourne l’adresse de la procédure de fenêtre d’origine pour la classe.

L’adresse de la procédure de fenêtre d’origine est utilisée dans le sous-processus global de la même façon que dans le sous-processus d’instance. La procédure de sous-classe transmet les messages à la procédure de fenêtre d’origine en appelant [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). L’application supprime la sous-classe de la classe de fenêtre en appelant à nouveau [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , en spécifiant l’adresse de la procédure de fenêtre d’origine, l’indicateur **\_ WNDPROC GCL** et le handle d’une fenêtre de la classe en cours de sous-classe. Une application qui sous-classe globalement une classe de contrôle doit supprimer la sous-classe lorsque l’application se termine ; dans le cas contraire, une erreur système irrécupérable peut se produire.

Le sous-classement global présente les mêmes limitations que le sous-modèle d’instance, ainsi que quelques restrictions supplémentaires. Une application ne doit pas utiliser les octets supplémentaires pour la classe ou l’instance de fenêtre sans connaître exactement la manière dont la procédure de fenêtre d’origine les utilise. Si l’application doit associer des données à une fenêtre, elle doit utiliser les propriétés de la fenêtre.

## <a name="window-procedure-superclassing"></a>Superclassement de la procédure de fenêtre

La *superclassement* est une technique qui permet à une application de créer une nouvelle classe de fenêtre avec les fonctionnalités de base de la classe existante, ainsi que les améliorations fournies par l’application. Une superclasse est basée sur une classe de fenêtre existante appelée *classe de base*. Souvent, la classe de base est une classe de fenêtre globale système telle qu’un contrôle d’édition, mais il peut s’agir de n’importe quelle classe de fenêtre.

Une superclasse a sa propre procédure de fenêtre, appelée procédure de superclasse. La *procédure de superclasse* peut prendre trois actions lors de la réception d’un message : elle peut passer le message à la procédure de fenêtre d’origine, modifier le message et le passer à la procédure de fenêtre d’origine, ou traiter le message et ne pas le passer à la procédure de fenêtre d’origine. Si la procédure de superclasse traite un message, elle peut le faire avant, après ou avant et après la transmission du message à la procédure de fenêtre d’origine.

Contrairement à une procédure de sous-classe, une procédure de superclasse peut traiter les messages de création de fenêtre ([**WM \_ NCCREATE**](wm-nccreate.md), [**WM \_ Create**](wm-create.md), etc.), mais elle doit également les transmettre à la procédure de fenêtre de la classe de base d’origine afin que la procédure de fenêtre de la classe de base puisse exécuter sa procédure d’initialisation.

Pour superclasser une classe de fenêtre, une application appelle d’abord la fonction [**GetClassinfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) pour récupérer des informations sur la classe de base. **GetClassinfo** remplit une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avec les valeurs de la structure **WNDCLASS** de la classe de base. Ensuite, l’application copie son propre handle d’instance dans le membre **HINSTANCE** de la structure **WNDCLASS** et copie le nom de la superclasse dans le membre **lpszClassName** . Si la classe de base a un menu, l’application doit fournir un nouveau menu avec les mêmes identificateurs de menu et copier le nom de menu dans le membre **lpszMenuName** . Si la procédure de superclasse traite le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) et ne la passe pas à la procédure de fenêtre de la classe de base, il n’est pas nécessaire que le menu ait des identificateurs correspondants. **GetClassinfo** ne retourne pas le membre **lpszMenuName**, **lpszClassName** ou **HINSTANCE** de la structure **WNDCLASS** .

Une application doit également définir le membre **lpfnWndProc** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . La fonction [**GetClassinfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) remplit ce membre avec l’adresse de la procédure de fenêtre d’origine pour la classe. L’application doit enregistrer cette adresse, transmettre les messages à la procédure de fenêtre d’origine, puis copier l’adresse de la procédure de superclasse dans le membre **lpfnWndProc** . L’application peut, si nécessaire, modifier tous les autres membres de la structure **WNDCLASS** . Après avoir rempli la structure **WNDCLASS** , l’application inscrit la superclasse en passant l’adresse de la structure à la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . La superclasse peut ensuite être utilisée pour créer des fenêtres.

Étant donné que la superclasse enregistre une nouvelle classe de fenêtre, une application peut ajouter à la fois les octets de classe supplémentaires et les octets de fenêtre supplémentaires. La superclasse ne doit pas utiliser les octets supplémentaires originaux pour la classe de base ou la fenêtre pour les mêmes raisons qu’une sous-classe d’instance ou une sous-classe globale ne doit pas les utiliser. En outre, si l’application ajoute des octets supplémentaires pour son utilisation à la classe ou à l’instance de fenêtre, elle doit référencer les octets supplémentaires par rapport au nombre d’octets supplémentaires utilisés par la classe de base d’origine. Étant donné que le nombre d’octets utilisés par la classe de base peut varier d’une version de la classe de base à l’autre, le décalage de départ pour les octets supplémentaires de la superclasse peut également varier d’une version de la classe de base à la suivante.

 

 
