---
description: Les messages sont définis dans un fichier texte de message. Le compilateur de message affecte des nombres à chaque message et génère un fichier include C/C++ que l’application peut utiliser pour accéder à un message à l’aide d’une constante symbolique.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: Fichiers texte du message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818210cfe58fb8eafe939c70a2a57b358e306bb9bc072a64abebbec5ca41c266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151475"
---
# <a name="message-text-files"></a>Fichiers texte du message

Les messages sont définis dans un fichier texte de message. Le compilateur de message affecte des nombres à chaque message et génère un fichier include C/C++ que l’application peut utiliser pour accéder à un message à l’aide d’une constante symbolique.

La syntaxe générale pour les instructions dans un fichier texte de message est la suivante :

*mot clé* = *valeur*

Les espaces autour du signe égal sont ignorés, et la valeur est délimitée par un espace blanc (y compris les sauts de ligne) de la paire mot clé/valeur suivante. La casse est ignorée lors de la comparaison des noms de mots clés. La partie *valeur* peut être une constante entière numérique à l’aide de la syntaxe c/c++, un nom de symbole qui respecte les règles pour les identificateurs c/c++, ou un nom de fichier comportant 8 caractères ou moins, sans points.

Pour obtenir un exemple de fichier de message, consultez [exemple de fichier texte de message](sample-message-text-file.md).

## <a name="comments"></a>Commentaires

Les lignes de commentaire sont autorisées dans le fichier texte du message. Un point-virgule (;) commence un commentaire qui se termine à la fin de la ligne. Suivez le point-virgule avec un indicateur de commentaire sur une seule ligne C/C++ (//) pour que le fichier d’en-tête généré par le compilateur de message soit compilé dans votre application.

``` syntax
;// This is a single-line comment.
```

Pour un commentaire de bloc, commencez chaque ligne par un point-virgule, puis placez un indicateur de commentaire de bloc ouvert C/C++ (/ \* ) après le point-virgule sur la première ligne et l’indicateur de commentaire de bloc de fermeture ( \* /) après le point-virgule sur la dernière ligne.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Section d'en-tête

Le fichier texte du message contient un en-tête qui définit les noms et les identificateurs de langue à utiliser par les définitions de message dans le corps du fichier. L’en-tête contient zéro, une ou plusieurs des instructions suivantes.



| Syntaxe d’instruction                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef =*type*                    | Type à utiliser dans la définition de message comme suit : \# define *Name* ((*type*) 0x *nnnnnnnn*)<br/> Le type doit être suffisamment grand pour contenir le code de message entier, tel qu’une **valeur DWORD**. Le type peut également être un type défini dans le code source de l’application. La valeur par défaut du *type* étant vide, aucun cast de type n’est utilisé. <br/> Cette instruction peut être spécifiée dans l’en-tête et aussi souvent que nécessaire dans la section Définition du message.<br/>                                                                                                                  |
| SeverityNames = (*nom* = *numéro* \[ :*nom* \] ) | Ensemble de noms autorisés pour la gravité dans une définition de message. Le nombre associé à chaque nom de gravité est un nombre qui, lorsqu’il est décalé de 30 bits vers la gauche, donne au modèle binaire la valeur logique ou avec les valeurs d’installation et d’ID de message pour former le code du message. Toute valeur de gravité qui ne tient pas dans 2 bits est une erreur. Les codes de gravité peuvent également recevoir des noms symboliques. La valeur par défaut est définie comme suit : SeverityNames = (Success = 0x0 informatif = 0x1 Warning = 0X2 Error = 0x3)<br/>                                                                      |
| FacilityNames = (*nom* = *numéro* \[ :*nom* \] ) | Ensemble de noms autorisés pour les valeurs d’installation dans une définition de message. Le nombre d’éléments associés à chaque nom de fonctionnalité est un nombre qui, en cas de décalage vers la gauche de 16 bits, donne au modèle binaire la valeur logique-ou avec les valeurs de gravité et d’ID de message pour former le code du message. Toute valeur de fonctionnalité qui ne tient pas dans 12 bits est une erreur. Cela permet d’obtenir des codes d’installation de 4096. les 256 premiers codes sont réservés à l’utilisation du système. Les codes d’installation peuvent également recevoir des noms symboliques. La valeur par défaut est définie comme suit : FacilityNames = (System = 0x0FF application = 0xFFF)<br/> |
| LanguageNames = ( = *numéro* de nom :*nom_fichier*) | Ensemble de noms autorisés pour les valeurs de langue dans une définition de message. Le nombre est utilisé comme identificateur de langue dans la table des ressources. Le fichier spécifié contient les messages pour cette langue. Il s’agit généralement d’un fichier. bin généré par le compilateur de message.<br/> Exemple de valeur : LanguageNames = (English = 0x40C : MSG00409)<br/> Pour obtenir la liste des identificateurs de langue, consultez <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase =*nombre*                        | Base de sortie pour les constantes de message que le compilateur de message écrit dans le fichier d’en-tête. S’il est présent, cette valeur remplace le commutateur-d. Ce nombre peut être 10 (décimal) ou 16 (hexadécimal).                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Définitions de message

Un fichier texte de message contient zéro, une ou plusieurs définitions de message après la section d’en-tête. Le tableau suivant décrit les instructions de définition de message. L’instruction MessageId marque le début de la définition du message. Les instructions de gravité et de fonction sont facultatives.



| Syntaxe d’instruction                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageID = numéro de \[ *numéro* \| + \] | Identificateur du message. Cette instruction est obligatoire, même si la valeur est facultative. Si aucune valeur n’est spécifiée, la valeur utilisée est la valeur précédente pour l’installation, plus une. Si la valeur est spécifiée avec un signe plus, la valeur utilisée est la valeur précédente pour l’installation, plus le nombre après le signe plus. Toute valeur spécifiée doit être contenue dans 16 bits. Pour plus d’informations sur la façon dont la valeur du message est formée à partir de la gravité, de l’installation et de l’ID de message, consultez le diagramme dans Winerror. h. Ce fichier d’en-tête définit les codes d’erreur du système.<br/> |
| Gravité =*nom*                   | L’une des valeurs spécifiées par SeverityNames dans l’en-tête. Cette instruction est facultative. Si aucune valeur n’est spécifiée, la valeur utilisée est la dernière valeur spécifiée pour une définition de message. La valeur par défaut de la première définition de message est `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Fonctionnalité =*nom*                   | L’une des valeurs spécifiées par FacilityNames dans l’en-tête. Cette instruction est facultative. Si aucune valeur n’est spécifiée, la valeur utilisée est la dernière valeur spécifiée pour une définition de message. La valeur par défaut de la première définition de message est `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| SymbolicName =*nom*               | Associe une constante symbolique C/C++ au code du message. Elle est utilisée dans la définition de message comme suit : \# define *Name* ((*type*) 0x *nnnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase = {*Number*}             | La base de sortie pour le message constantes le compilateur de messages écrit dans le fichier d’en-tête. S’il est présent, cette valeur remplace le commutateur-d. Ce nombre peut être 10 (décimal) ou 16 (hexadécimal).                                                                                                                                                                                                                                                                                                                                                                 |
| Language =*nom*                   | L’une des valeurs spécifiées par LanguageNames dans l’en-tête. Cette instruction est facultative. Si aucune valeur n’est spécifiée, la valeur utilisée est la dernière valeur spécifiée pour une définition de message. La valeur par défaut de la première définition de message est la suivante : `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *texte du message*                    | Texte du message. Il est inclus dans le fichier binaire du message. Il est également inclus dans le fichier d’en-tête dans le bloc de commentaires qui précède directement la définition du message.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | Le texte du message se termine par une nouvelle ligne contenant un point unique au début de la ligne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Si la définition du message comprend un texte de message pour plusieurs langues, chaque langue requiert son propre instruction de langue, son texte de message et la nouvelle ligne de fin avec un point. Par exemple :

``` syntax
MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.
```

Vous pouvez spécifier les séquences d’échappement suivantes pour mettre en forme le texte du message en vue de son utilisation par l’observateur d’événements ou votre application. Le signe de pourcentage (%) commence toutes les séquences d’échappement. Tout autre caractère qui suit un signe de pourcentage est affiché sans le signe de pourcentage.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *\_ spécificateur de format*!\]
</dt> <dd>

Décrit une insertion. Chaque insertion est une entrée dans le tableau d’arguments de la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . La valeur de *n* peut être un nombre compris entre 1 et 99. Le spécificateur de format est facultatif. Si aucune valeur n’est spécifiée, la valeur par défaut est ! s !. Pour plus d’informations sur le spécificateur de format, consultez [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

Le spécificateur de format peut être utilisé \* pour la précision ou la largeur. Lorsqu’ils sont spécifiés, ils consomment des insertions numérotées *n*+ 1 et *n*+ 2.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Met fin à une ligne de texte de message sans caractère de saut de ligne de fin. Cela peut être utilisé pour générer une longue ligne ou mettre fin à un message d’invite sans caractère de saut de ligne de fin.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Génère une seule période. Cela peut être utilisé pour afficher un point au début d’une ligne, qui, sinon, termine le texte du message.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Génère un point d’exclamation unique. Cela peut être utilisé pour spécifier un point d’exclamation immédiatement après une insertion.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Génère un signe de pourcentage unique.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>% n
</dt> <dd>

Génère un saut de ligne physique lorsqu’il se produit à la fin d’une ligne. Vous pouvez l’utiliser avec [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) pour vous assurer que le message correspond à une certaine largeur.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>% b
</dt> <dd>

Génère un espace. Cela peut être utilisé pour garantir un nombre approprié d’espaces à droite sur une ligne.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>% r
</dt> <dd>

Génère un retour chariot sans caractère de saut de ligne de fin.

</dd> </dl>

 

