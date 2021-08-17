---
title: considérations sur la sécurité contrôles Microsoft Windows
description: cette rubrique fournit des informations sur les considérations relatives à la sécurité pour les contrôles Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45faa0f3d2f521038c056055329d70541625bac88c16e62c1581b55ae2a6c5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696509"
---
# <a name="security-considerations-microsoft-windows-controls"></a>considérations relatives à la sécurité : contrôles Microsoft Windows

cette rubrique fournit des informations sur les considérations relatives à la sécurité pour les contrôles Windows. Les informations contenues dans cette rubrique ne fournissent pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-la comme point de départ et référence pour ce domaine technologique.

L’interconnexion entre les ordinateurs est courante. la principale préoccupation d’un développeur doit être la sécurité des applications. les sections suivantes présentent certains problèmes de sécurité potentiels à prendre en compte lors de la programmation de contrôles Windows.

-   [Messages de contrôle se terminant par null](#null-terminated-control-messages)
-   [Utilisation de chaîne](#string-use)
-   [Validation des entrées](#input-validation)
-   [Utilisation du mot de passe](#password-use)
-   [alertes de sécurité](#security-alerts)
-   [Rubriques connexes](#related-topics)

## <a name="null-terminated-control-messages"></a>Messages de contrôle se terminant par null

La plupart des messages de contrôle et des macros ont des paramètres de chaîne. Souvent, ces messages ne valident pas les chaînes d’entrée, en particulier, elles ne vérifient pas la fin d’une opération `'\0'` . Lorsque vous appelez un message qui utilise une chaîne comme paramètre, spécifiez explicitement que la chaîne se termine par un caractère null.

## <a name="string-use"></a>Utilisation de chaîne

quand vous programmez des contrôles Windows, il est nécessaire de manipuler des chaînes. Presque tous les contrôles requièrent l’insertion de texte. Par exemple, pour remplir une zone de liste, vous devez charger des chaînes dans le contrôle. Étant donné que l’utilisation de chaînes de manière incorrecte provoque souvent des dépassements de mémoire tampon, prenez des précautions pour éviter ce risque de sécurité.

Pour plus d’informations sur les dépassements de mémoire tampon, consultez *écriture de code sécurisé* par Michael Howard et David LeBlanc, Microsoft Press, 2002 et [meilleures pratiques pour les API de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>Validation d'entrée

Les messages de contrôle suivants peuvent présenter des problèmes de sécurité.

-   [**\_GETLBTEXT CB**](cb-getlbtext.md)
-   [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md)
-   [**SB \_ GETTEXT**](sb-gettext.md)
-   [**\_GETTIPTEXT SB**](sb-gettiptext.md)
-   [**TO \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**ATTÉNUATION \_ GETTEXT**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

Si le texte change entre l’appel pour obtenir la longueur du texte et l’heure d’affichage ou d’utilisation du texte, un dépassement de mémoire tampon peut se produire. Pour éviter cela, vous devez valider la chaîne avant de l’utiliser. En outre, les messages qui extraient Text, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**to \_ GETBUTTONTEXT**](tb-getbuttontext.md)et [**atténuation \_ GETTEXT**](ttm-gettext.md), n’ont pas de paramètre de taille de mémoire tampon qui présente le risque de dépassement de mémoire tampon.

Quand vous utilisez [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou [**SB \_ GETTEXT**](sb-gettext.md), vous devez d’abord appeler [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) ou [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour obtenir la taille de la mémoire tampon. Certains de ces messages, [**to \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)et [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)peuvent être appelés avec une valeur de paramètre **null** pour obtenir la longueur de la chaîne avant d’appeler le message pour récupérer la chaîne.

Un message dont vous devez prêter une attention particulière est le message de la barre d’état [**SB \_ GETTIPTEXT**](sb-gettiptext.md) . Ce message n’offre aucun moyen d’interroger la longueur de la chaîne qui doit être récupérée.

## <a name="password-use"></a>Utilisation du mot de passe

Si vous utilisez des contrôles d’édition protégés par mot de passe (style [**\_ de mot de passe es**](edit-control-styles.md) ), la mémoire tampon qui contient le texte récupéré doit avoir la valeur zéro dès que possible pour éviter d’exposer le mot de passe de l’utilisateur en mémoire.

## <a name="security-alerts"></a>Alertes de sécurité

Le tableau suivant répertorie les fonctionnalités qui, si elles sont utilisées de manière incorrecte, peuvent compromettre la sécurité de vos applications. Les messages répertoriés ici ne fournissent pas de paramètre spécifiant la taille de la mémoire tampon.



| Fonctionnalité                                               | Limitation des risques                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Assurez-vous que la mémoire tampon utilisée par la fonction peut être écrite dans et qu’elle se termine par un caractère null.                                                                     |
| [**\_GETLBTEXT CB**](cb-getlbtext.md)                 | Appelez [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) pour obtenir la taille de la mémoire tampon, puis appelez [**CB \_ GETLBTEXT**](cb-getlbtext.md) pour récupérer la chaîne. |
| [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md) | Appelez le message avec une valeur de paramètre **null** pour obtenir la taille de la mémoire tampon, puis appelez le message une deuxième fois pour récupérer la chaîne.             |
| [**SB \_ GETTEXT**](sb-gettext.md)                     | Appelez [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour obtenir la taille de la mémoire tampon, puis appelez [**SB \_ GETTEXT**](sb-gettext.md) pour récupérer la chaîne.   |
| [**TO \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Appelez le message avec une valeur de paramètre **null** pour obtenir la taille de la mémoire tampon, puis appelez le message une deuxième fois pour récupérer la chaîne.             |
| [**ATTÉNUATION \_ GETTEXT**](ttm-gettext.md)                   | Ce message n’offre aucun moyen de connaître ou de spécifier la taille de la mémoire tampon.                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | Appelez le message en passant une valeur de paramètre **null** pour obtenir la taille de la mémoire tampon, puis appelez le message une seconde fois pour récupérer la chaîne.       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Autres ressources**
</dt> <dt>

[Sécurité Microsoft](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Sécurité](/windows/desktop/security)
</dt> <dt>

[Ressources de sécurité TechNet](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Meilleures pratiques pour les API de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 