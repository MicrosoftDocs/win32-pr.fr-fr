---
description: Les développeurs qui créent des applications pour Tablet PC peuvent tirer parti de l’étendue des entrées et des informations de contexte.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Utilisation du contexte par la plateforme Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c586bf3ffcff8fc92b02bc0b4f5aff79c6bd0bbd66e6f048eab35a78d3be9676
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709279"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Utilisation du contexte par la plateforme Tablet PC

Les développeurs qui créent des applications pour Tablet PC peuvent tirer parti de l’étendue des entrées et des informations de contexte. Les meilleures solutions possibles pour définir des informations de contexte sur les contrôles dans les applications varient selon que le contrôle est activé pour l’entrée manuscrite et que l’application a été publiée sur le marché. Un contrôle avec accès manuscrit est un contrôle spécifiquement conçu pour l’entrée d’encre et dans lequel les données d’encre sont principalement collectées et conservées en tant qu’encre. Microsoft Windows Journal ou un programme d’esquisse sont des exemples d’applications compatibles avec l’écriture manuscrite. Dans un contrôle qui n’est pas activé pour l’écriture manuscrite, les données d’entrée sont collectées et conservées en tant que texte, en général à l’aide du panneau de saisie Tablet PC lorsque l’application est exécutée sur un Tablet PC. Les solutions permettant d’activer les informations de contexte dans les contrôles sont les suivantes :

-   API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) : solution de programmation de bas niveau pour les applications et les contrôles qui ne sont pas compatibles avec l’encre. Les fichiers binaires de l’application sont affectés et doivent être redistribués.
-   Propriétés [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) [**et de la**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) zone de texte de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) : solution de programmation pour les applications avec des contrôles activés pour l’écriture manuscrite. Les fichiers binaires de l’application sont affectés et doivent être redistribués.

le panneau de saisie Tablet pc a été mis à jour à partir de Windows Vista pour tirer parti des informations de contexte que vous fournissez lors de l’utilisation des api [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) . Le tableau suivant fournit des détails sur les moteurs de reconnaissance Microsoft qui prennent en charge les étendues d’entrée. Un « X » dans la ligne d’une étendue d’entrée indique que le module de reconnaissance dans cette colonne prend en charge l’étendue des entrées.



| Nom de la propriété                                     | Anglais (États-Unis) | Anglais (Royaume-Uni) | Allemand       | Français       | Japonais     | Coréen       | Chinois (simplifié) | Chinois (traditionnel) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **EST l' \_ adresse \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST l' \_ adresse \_ POSTALCODE**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_adresse \_ postale**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST l' \_ adresse \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST la ville de l' \_ adresse \_**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST l' \_ adresse \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST l' \_ adresse \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST une \_ devise \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ un \_ montant en devise**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ date \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST la \_ date \_ mois**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST la \_ date \_ jour**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST la date de l' \_ \_ année**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ date \_ MonthName**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ date \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST la \_ valeur par défaut**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_ \_ nom d’utilisateur de l’e-mail**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_SMTPEMAILADDRESS e-mail \_**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ fichier \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_ \_ nom du fichier**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ LOGINNAME**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ chiffre**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ nombre**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ mot de passe**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ PERSONALNAME \_ FullName**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ un \_ préfixe PERSONALNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_nom du PERSONALNAME \_**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ un \_ suffixe PERSONALNAME**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ téléphone \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST le pays de la \_ compagnie \_**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ un \_ indicatif téléphonique**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ téléphone \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ Time \_ FullTime**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ une \_ heure**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ heure \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST une \_ URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST un \_ nombre \_ pleine chasse**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ une \_ demi-chasse alphanumérique**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ \_ pleine chasse**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST une \_ devise \_ chinoise**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ bopomofo**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST en \_ hiragana**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ Katakana \_ demi-chasse**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ une \_ pleine chasse katakana**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **EST \_ Hanja**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Lorsque vous utilisez les API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) ou la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) pour définir le contexte, la tentative de définition d’une étendue d’entrée pour une langue qui n’est pas prise en charge par le module de reconnaissance de ce langage entraîne l’utilisation du modèle de langue par défaut comme contexte du contrôle par le panneau de saisie du Tablet PC. Par exemple, l’étendue de l’entrée de l' **\_ adresse \_ STATEORPROVINCE** n’est pas prise en charge par le module de reconnaissance français. Si vous définissez le contexte sur un champ en tant que

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

lors de l’utilisation du module de reconnaissance français, le contexte résultant est le modèle de langue par défaut. Pour éviter ce problème, détectez la langue du module de reconnaissance en cours d’utilisation et définissez les étendues d’entrée en conséquence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

