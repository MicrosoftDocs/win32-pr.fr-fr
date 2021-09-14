---
title: E (menus et autres ressources)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220788"
---
# <a name="e-menus-and-other-resources"></a>E (menus et autres ressources)

[A](a.md) [B](b.md) [C](c.md) D e [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menus vides non autorisés**
</dt> <dd>

Un mot clé **end** apparaît avant que tous les éléments de menu ne soient définis dans l’instruction de [**menu**](menu-resource.md) . les menus vides ne sont pas autorisés par le compilateur de ressources Microsoft Windows 32 (RC). Assurez-vous que vous n’avez pas de guillemets ouvrants dans l’instruction de **menu** .

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Fin attendue dans la boîte de dialogue**
</dt> <dd>

Le mot clé **end** doit apparaître à la fin d’une instruction [**Dialog**](dialog-resource.md) . Assurez-vous qu’il n’y a pas de guillemets ouvrants à gauche de l’instruction précédente.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END attendu dans le menu**
</dt> <dd>

Le mot clé **end** doit apparaître à la fin d’une instruction de [**menu**](menu-resource.md) . Assurez-vous qu’il n’y a pas d’instructions **Begin** et **end** incompatibles.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Nom d’erreur Creatingresource**
</dt> <dd>

le compilateur de ressources Microsoft Windows 32 (RC) n’a pas pu créer la ressource binaire spécifiée (. RES). Assurez-vous qu’il n’est pas créé sur un lecteur en lecture seule. Utilisez l’option **/v** pour déterminer si le fichier est en cours de création.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Virgule attendue dans la table d’accélérateurs**
</dt> <dd>

le compilateur de ressources Microsoft Windows 32 (RC) requiert une virgule entre les paramètres *event* et *idvalue* dans l’instruction [**accelerators**](accelerators-resource.md) .

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Nom de classe de contrôle ATTENDU**
</dt> <dd>

Le paramètre de *classe* d’une instruction de [**contrôle**](control-control.md) dans l’instruction [**Dialog**](dialog-resource.md) doit être de l’un des types de contrôle suivants : **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** ou défini par l’utilisateur. Assurez-vous que la classe est correctement orthographiée.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nom de type de police ATTENDU**
</dt> <dd>

Le paramètre *Typeface* de l’instruction **font** dans l’instruction [**Dialog**](dialog-resource.md) doit être une chaîne de caractères placée entre guillemets doubles ("). Ce paramètre spécifie le nom d’une police.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Valeur d’ID attendue pour MenuItem**
</dt> <dd>

L’instruction [**menu**](menu-resource.md) doit contenir une instruction [**MenuItem**](menuitem-statement.md) , qui a soit un entier, soit une constante symbolique dans le paramètre *menuID* .

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Chaîne de menu attendue**
</dt> <dd>

Chaque instruction [**MenuItem**](menuitem-statement.md) et [**Popup**](popup-resource.md) doit contenir un paramètre de *texte* . Ce paramètre est une chaîne placée entre guillemets doubles (") qui spécifie le nom de l’élément de menu ou du menu contextuel. Une instruction de **séparateur MenuItem** ne requiert pas de chaîne entre guillemets.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valeur de commande numérique attendue**
</dt> <dd>

Microsoft Windows resource Compiler (RC) attendait un paramètre *idvalue* numérique dans l’instruction [**accelerators**](accelerators-resource.md) . Assurez-vous que vous avez utilisé une instruction de [**\# définition**](-define.md) pour spécifier la valeur et que la constante utilisée est correctement orthographiée.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Constante numérique attendue dans la table de chaînes**
</dt> <dd>

Une constante numérique, définie dans une instruction de [**\# définition**](-define.md) , doit suivre immédiatement le mot clé **Begin** dans une instruction [**STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Taille de point numérique attendue**
</dt> <dd>

Le *paramètre Resize* de l’instruction [**font**](font-statement.md) dans l’instruction [**Dialog**](dialog-resource.md) doit être une valeur de taille de point entière.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Constante de boîte de dialogue numérique attendue**
</dt> <dd>

Une instruction [**Dialog**](dialog-resource.md) requiert des valeurs entières pour les paramètres *x*, *y*, *Width* et *Height* . Assurez-vous que ces valeurs, qui sont incluses après le mot clé **Dialog** , ne sont pas négatives.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Chaîne attendue dans STRINGTABLE**
</dt> <dd>

Une chaîne est attendue après chaque paramètre *stringid* numérique dans une instruction [**STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Commande d’accélérateur de constante ou de chaîne attendue**
</dt> <dd>

Microsoft Windows resource Compiler (RC) n’a pas pu déterminer la clé qui était configurée pour l’accélérateur. Le paramètre d' *événement* de l’instruction [**Accelerators**](accelerators-resource.md) n’est peut-être pas valide.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**VALEUR, bloc ou mot clé END attendu.**
</dt> <dd>

La structure [**VERSIONINFO**](versioninfo-resource.md) requiert un mot clé de **valeur**, de **bloc** ou de **fin** .

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Nombre attendu pour l’ID**
</dt> <dd>

Un nombre est attendu pour le paramètre *ID* d’une instruction [**Control**](control-control.md) dans l’instruction [**Dialog**](dialog-resource.md) . Assurez-vous de disposer d’un nombre ou d’une instruction de [**\# définition**](-define.md) pour l’identificateur du contrôle.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Chaîne entre guillemets attendue pour la clé**
</dt> <dd>

La chaîne de clé qui suit le mot clé **Block** ou **value** doit être placée entre guillemets doubles.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Chaîne entre guillemets attendue dans la classe Dialog**
</dt> <dd>

Le paramètre *Class* de l’instruction [**Class**](class-statement.md) de l’instruction [**Dialog**](dialog-resource.md) doit être un entier ou une chaîne placée entre guillemets doubles (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Chaîne entre guillemets attendue dans le titre de la boîte de dialogue**
</dt> <dd>

Le paramètre *CaptionText* de l’instruction [**Caption**](caption-statement.md) dans l’instruction [**Dialog**](dialog-resource.md) doit être une chaîne de caractères placée entre guillemets doubles (").

</dd> </dl>

 

 




