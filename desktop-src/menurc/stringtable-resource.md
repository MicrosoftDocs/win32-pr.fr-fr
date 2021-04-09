---
title: Ressource STRINGTABLE
description: Définit une ou plusieurs ressources de type chaîne pour une application. Les ressources de type chaîne sont simplement des chaînes Unicode ou ASCII se terminant par un caractère null qui peuvent être chargées quand cela est nécessaire à partir du fichier exécutable, à l’aide de la fonction LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menus des ressources STRINGTABLE et autres ressources
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101628"
---
# <a name="stringtable-resource"></a>Ressource STRINGTABLE

Définit une ou plusieurs ressources de type chaîne pour une application. Les ressources de type chaîne sont simplement des chaînes Unicode ou ASCII se terminant par un caractère null qui peuvent être chargées quand cela est nécessaire à partir du fichier exécutable, à l’aide de la fonction [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .

Il existe deux façons de mettre en forme une instruction **STRINGTABLE** :

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- ou -

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*
</dt> <dd>

Ce paramètre peut être égal à zéro ou plusieurs des instructions suivantes.



| .                                                        | Description                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caractéristiques**](characteristics-statement.md) *DWORD*     | Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources. Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md). |
| [](language-statement.md) *Langue* langue, sous- *langue* | Spécifie la langue de la ressource. Pour plus d’informations, consultez [**Language**](language-statement.md).                                                                              |
| [**Version**](version-statement.md) *DWORD*                     | Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources. Pour plus d’informations, consultez [**version**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

Entier non signé 16 bits qui identifie la ressource.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*chaîne*
</dt> <dd>

Une ou plusieurs chaînes, placées entre guillemets. La chaîne ne doit pas dépasser 4097 caractères et doit occuper une seule ligne dans le fichier source. Pour ajouter un retour chariot à la chaîne, utilisez la séquence de caractères suivante : \\ 012. Par exemple, « ligne un \\ 012Line deux » définit une chaîne qui s’affiche comme suit :

``` syntax
Line one
Line two
```

Pour incorporer des guillemets dans la chaîne, utilisez la séquence suivante : "". Par exemple, "" ", ligne trois" ", définit une chaîne qui s’affiche comme suit :

``` syntax
"Line three"
```

Pour encoder des caractères Unicode, utilisez un « L » suivi des caractères Unicode encadrés par des guillemets. Pour obtenir un exemple, consultez la section exemples.

Le compilateur de ressources prend également en charge les continuations de ligne dans *String*. Pour obtenir un exemple, consultez la section exemples.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Notes

RC alloue 16 chaînes par section et utilise la valeur d’identificateur pour déterminer la section qui doit contenir la chaîne. Les chaînes dont les identificateurs diffèrent uniquement dans les 4 bits inférieurs sont placées dans la même section. Pour plus d’informations, consultez [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **STRINGTABLE** pour afficher des chaînes ASCII :

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

L’exemple suivant montre comment encoder des caractères Unicode :

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

L’exemple suivant montre des chaînes avec ASCII et Unicode. Notez que les chaînes sans la « L » initiale utilisent le format d’échappement à 2 chiffres :

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

L’exemple suivant montre comment les continuations de ligne peuvent être utilisées :

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 