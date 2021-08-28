---
title: Chaînes
description: Cette section décrit les fonctions de chaîne.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- ressources, chaînes
- chaînes
- fonctions de chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3799c151b828dba1d687068da6f7f5924aded09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478895"
---
# <a name="strings"></a>Chaînes

Cette section décrit les fonctions de chaîne et explique comment les utiliser dans vos applications.

### <a name="in-this-section"></a>Dans cette section



| Name                                     | Description                                             |
|------------------------------------------|---------------------------------------------------------|
| [À propos des chaînes](about-strings.md)       | Décrit les fonctions de chaîne.<br/>              |
| [À propos de strsafe. h](strsafe-ovw.md)       | Décrit les fonctions de chaîne dans strsafe. h.<br/> |
| [Référence de chaîne](string-reference.md) | Contient la référence de l’API.<br/>                  |



 

### <a name="string-functions"></a>Fonctions de chaîne




| Name | Description | 
|------|-------------|
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a> | Convertit une chaîne de caractères ou un caractère unique en minuscules. Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a> | Convertit les caractères majuscules d’une mémoire tampon en caractères minuscules. La fonction convertit les caractères sur place. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a> | Récupère un pointeur vers le caractère suivant dans une chaîne. Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a> | Récupère le pointeur vers le caractère suivant dans une chaîne. Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a> | Récupère un pointeur vers le caractère précédent dans une chaîne. Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a> | Récupère le pointeur désignant le caractère précédent dans une chaîne. Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> | Convertit une chaîne en jeu de caractères défini par l’OEM.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a> | Convertit un nombre spécifié de caractères dans une chaîne en jeu de caractères défini par l’OEM.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a> | Convertit une chaîne de caractères ou un seul caractère en majuscules. Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a> | Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules. La fonction convertit les caractères sur place. <br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> | Compare deux chaînes de caractères, à l’aide des paramètres régionaux spécifiés.<blockquote>[!Note]<br />Pour la compatibilité avec Unicode, utilisez <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> ou la version Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> | Compare deux chaînes Unicode (caractères larges) à l’aide des paramètres régionaux spécifiés.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString devant</strong></a> | Cartes une chaîne à une autre, en effectuant une option de transformation spécifiée. <br /> | 
| <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> | Récupère des informations de type caractère pour les caractères de la chaîne source spécifiée. Pour chaque caractère de la chaîne, la fonction définit un ou plusieurs bits dans l’élément 16 bits correspondant du tableau de sortie. Chaque bit identifie un type de caractère donné, par exemple si le caractère est une lettre, un chiffre ou aucun des deux.<br /> | 
| <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> | Récupère des informations de type caractère pour les caractères de la chaîne source spécifiée. Pour chaque caractère de la chaîne, la fonction définit un ou plusieurs bits dans l’élément 16 bits correspondant du tableau de sortie. Chaque bit identifie un type de caractère donné, par exemple si le caractère est une lettre, un chiffre ou aucun des deux. <br /> Contrairement à ses parents proches <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> et <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> présente un comportement standard grâce à l’utilisation du commutateur <strong>#define Unicode</strong> . Il s’agit de la fonction recommandée.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a> | Récupère des informations de type caractère pour les caractères de la chaîne source spécifiée. Pour chaque caractère de la chaîne, la fonction définit un ou plusieurs bits dans l’élément 16 bits correspondant du tableau de sortie. Chaque bit identifie un type de caractère donné, par exemple si le caractère est une lettre, un chiffre ou aucun des deux.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a> | Détermine si un caractère est un caractère alphabétique. Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a> | Détermine si un caractère est un caractère alphabétique ou numérique. Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a> | Détermine si un caractère est en minuscules. Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a> | Détermine si un caractère est en majuscules. Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a> | Charge une ressource de chaîne à partir du fichier exécutable associé à un module spécifié, copie la chaîne dans une mémoire tampon et ajoute un caractère NULL de fin.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a> | Ajoute une chaîne à une autre.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a> | Compare deux chaînes de caractères. La comparaison respecte la casse.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a> | Compare deux chaînes de caractères. La comparaison ne respecte pas la casse.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a> | Copie une chaîne dans une mémoire tampon.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a> | Copie un nombre spécifié de caractères d’une chaîne source dans une mémoire tampon. <br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a> | Détermine la longueur de la chaîne spécifiée (à l’exclusion du caractère null de fin).<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a> | Convertit une chaîne du jeu de caractères défini par l’OEM en une chaîne ANSI ou à caractères larges.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a> | Convertit un nombre spécifié de caractères dans une chaîne du jeu de caractères défini par l’OEM en une chaîne de caractères ANSI ou larges.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a> | Écrit des données mises en forme dans la mémoire tampon spécifiée.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a> | Écrit des données mises en forme dans la mémoire tampon spécifiée à l’aide d’un pointeur vers une liste d’arguments.<br /> | 




 

### <a name="strsafe-functions"></a>Fonctions strsafe



| Name                                             | Description                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Concatène une chaîne à une autre chaîne.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Concatène une chaîne à une autre chaîne.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Concatène le nombre spécifié d’octets d’une chaîne à une autre chaîne.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Concatène le nombre spécifié d’octets d’une chaîne à une autre chaîne.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Copie une chaîne dans une autre.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Copie une chaîne dans une autre.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Copie le nombre d’octets spécifié d’une chaîne vers une autre.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Copie le nombre d’octets spécifié d’une chaîne vers une autre.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Détermine si une chaîne dépasse la longueur spécifiée, en octets.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Écrit des données mises en forme dans la chaîne spécifiée.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Écrit des données mises en forme dans la chaîne spécifiée.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Concatène une chaîne à une autre chaîne.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Concatène une chaîne à une autre chaîne.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Concatène le nombre spécifié de caractères d’une chaîne à une autre chaîne.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Concatène le nombre spécifié de caractères d’une chaîne à une autre chaîne.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Copie une chaîne dans une autre.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Copie une chaîne dans une autre.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Copie le nombre spécifié de caractères d’une chaîne vers une autre.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Copie le nombre spécifié de caractères d’une chaîne vers une autre.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Détermine si une chaîne dépasse la longueur spécifiée, en caractères.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Écrit des données mises en forme dans la chaîne spécifiée.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Écrit des données mises en forme dans la chaîne spécifiée.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.<br/> |



 

 

