---
title: Ressource ACCÉLÉRATEURs
description: Définit un ou plusieurs accélérateurs pour une application. Un accélérateur est une séquence de touches définie par l’application pour offrir à l’utilisateur un moyen rapide d’effectuer une tâche.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menus des ressources des ACCÉLÉRATEURs et autres ressources
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235746"
---
# <a name="accelerators-resource"></a>Ressource ACCÉLÉRATEURs

Définit un ou plusieurs accélérateurs pour une application. Un accélérateur est une séquence de touches définie par l’application pour offrir à l’utilisateur un moyen rapide d’effectuer une tâche.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits qui identifie la ressource.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*
</dt> <dd>

Zéro, une ou plusieurs des instructions suivantes.



| .                                                        | Description                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caractéristiques**](characteristics-statement.md) *DWORD*     | Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources. Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md). |
| [](language-statement.md) *Langue* langue, sous- *langue* | Spécifie la langue de la ressource. Pour plus d’informations, consultez [**Language**](language-statement.md).                                                                              |
| [**Version**](version-statement.md) *DWORD*                     | Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources. Pour plus d’informations, consultez [**version**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*événement*
</dt> <dd>

Séquence de touches à utiliser comme accélérateur. Il peut s’agir de l’un des types de caractères suivants.



| Type                    | Description                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| «*char*»                | Caractère unique placé entre guillemets doubles ("). Le caractère peut être précédé d’un signe insertion (^), ce qui signifie que le caractère est un caractère de contrôle.                                                                                  |
| *Caractère*             | Valeur entière représentant un caractère. Le paramètre de *type* doit être **ASCII**.                                                                                                                                                           |
| *caractère de clé virtuelle* | Valeur entière représentant une clé virtuelle. La clé virtuelle pour les clés alphanumériques peut être spécifiée en plaçant la lettre majuscule ou le nombre entre guillemets doubles (par exemple, « 9 » ou « C »). Le paramètre de *type* doit être **VIRTKEY**. |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idValue*
</dt> <dd>

valeur entière 16 bits non signée qui identifie l’accélérateur.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*entrer*
</dt> <dd>

Obligatoire uniquement lorsque le paramètre d' *événement* est un *caractère* ou un *caractère de clé virtuelle*. Le paramètre de *type* spécifie **ASCII** ou **VIRTKEY**. la valeur entière de l' *événement* est interprétée en conséquence. Lorsque **VIRTKEY** est spécifié et que *Event* contient une chaîne, l' *événement* doit être en majuscules.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Options*
</dt> <dd>

options qui définissent l’accélérateur. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Option                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Noinversé**                       | Spécifie qu’aucun élément de menu de niveau supérieur n’est mis en surbrillance lorsque l’accélérateur est utilisé. Cela est utile lorsque vous définissez des accélérateurs pour des actions telles que le défilement qui ne correspondent pas à un élément de menu. Si **noinversé** est omis, un élément de menu de niveau supérieur est mis en surbrillance (si possible) quand l’accélérateur est utilisé. Cet attribut est obsolète et conservé uniquement à des fins de compatibilité descendante avec les fichiers de ressources conçus pour une Windows 16 bits. |
| **Alt**                            | Entraîne l’activation de l’accélérateur uniquement si la touche ALT est enfoncée. S’applique uniquement aux clés virtuelles.                                                                                                                                                                                                                                                                                                                                            |
| **MAJUSCULE**                          | Entraîne l’activation de l’accélérateur uniquement si la touche Maj est enfoncée. S’applique uniquement aux clés virtuelles                                                                                                                                                                                                                                                                                                                                           |
| [**RÉGULATION**](control-control.md) | Définit le caractère en tant que caractère de contrôle (l’accélérateur est activé uniquement si la touche de contrôle est enfoncée). Cela a le même effet que l’utilisation d’un signe insertion (^) avant le caractère d’accélérateur dans le paramètre d' *événement* . S’applique uniquement aux clés virtuelles                                                                                                                                                                                           |



 

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Notes

La fonction [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) est utilisée pour convertir les messages d’accélérateur de la file d’attente de l’application en messages de [**\_ commande WM**](./wm-command.md) ou [**WM \_ SYSCOMMAND**](./wm-syscommand.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de touches accélérateur.

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des accélérateurs clavier](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**DIALOGUE**](dialog-resource.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSION**](version-statement.md)
</dt> </dl>

 

 