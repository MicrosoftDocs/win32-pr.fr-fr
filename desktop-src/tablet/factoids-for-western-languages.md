---
description: Les langues occidentales sont définies pour l’anglais (Royaume-Uni), l’anglais (États-Unis), le français, l’allemand et l’espagnol.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factoids pour les langues occidentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e417c9662252213d761760a1486f9808a2d18bc3236073fe8c8d7746c396beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936539"
---
# <a name="factoids-for-western-languages"></a>Factoids pour les langues occidentales

Les langues occidentales sont définies pour l’anglais (Royaume-Uni), l’anglais (États-Unis), le français, l’allemand et l’espagnol. Les formats de chaque Factoid répertoriés dans le tableau ci-dessous sont spécifiques au module de reconnaissance de chaque langue. Par exemple, le Factoid **téléphonique** est différent dans chaque langue. En outre, chaque Factoid est spécifique à un module de reconnaissance particulier. Par exemple, le Factoid **téléphonique** français peut être utilisé uniquement avec le module de reconnaissance français.

> [!Note]  
> En plus des Factoids suivants, tous les langages utilisent le Factoids listé dans [Factoids common dans plusieurs langues](factoids-common-across-languages.md).

 



| Factoid              | Définition                                                                                                                                                                                                                                                                                                                                                                                                           | Exemples                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nom du fichier**         | Définit le décalage pour un chemin d’accès au nom de fichier. Le nom ne peut pas contenir les caractères<br/> /" < > \|<br/> Les caractères \* et ? sont inclus dans ce Factoid pour permettre la recherche. En outre, les caractères étendus sont pris en charge dans les langues européennes.<br/>                                                                                                                                                    | c:<br/> \\\\\\nom du fichier DirectoryName<br/> \\\\\\nom de \\ fichier directory1 directory2<br/> \\\\DirectoryName \\ \* .\*<br/> nom de fichier. ?<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Active le dictionnaire système uniquement. Cela est utile si une application demande si un mot se trouve dans le dictionnaire système. Affectez à Factoid la valeur **SystemDictionary** et appelez la méthode [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) .<br/>                                                                                                                                                 | Le modèle de langue par défaut comprend la grammaire pour le langage ainsi que le dictionnaire système. Ce Factoid biais la reconnaissance vers uniquement les mots qui se produisent dans le dictionnaire système. Chaque langage possède son propre dictionnaire système.<br/>                   |
| **Mots**         | Active uniquement la liste de mots. Si Factoid a la valeur liste de **mots** , mais qu’aucune liste de mots n’est assignée au [**InkRecognizerContext**](inkrecognizercontext-class.md) ([RecognizerContext](/previous-versions/ms552546(v=vs.100)) dans le code managé), le dictionnaire de l’utilisateur est utilisé. Pour plus d’informations sur les listes de mots et les dictionnaires, consultez [utilisation de dictionnaires d’applications](using-application-dictionaries.md).<br/> | Ce Factoid biais le module de reconnaissance pour retourner uniquement les mots de la liste de mots. Par exemple, pour permettre à l’utilisateur d’entrer une couleur dans un formulaire, vous pouvez utiliser ce Factoid et une liste de mots contenant « vert », « rouge », « bleu », « blanc » et d’autres couleurs.<br/> |



 

Les combinaisons de Factoids suivantes sont prises en charge uniquement pour les langues occidentales. Les autres combinaisons de Factoids ne sont pas prises en charge dans cette version des interfaces de programmation d’applications (API) de la plateforme Tablet PC. Ces combinaisons Factoid utilisent un opérateur **or** logique. par conséquent, l’entrée peut correspondre à n’importe laquelle des Factoids de l’expression.



| Combinaison Factoid     | Définition                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **WebWordList**         | Factoid **Web** ou liste de mots.<br/>                             |
| **EmailWordList**       | Factoid d' **e-mail** ou liste de mots.<br/>                           |
| **FilenameWebWordList** | **Nom de fichier** Factoid ou Factoid **Web** ou liste de mots.<br/> |



 

Les rubriques suivantes présentent les formats pris en charge pour chaque langue de l’Ouest.

-   [Anglais (Worldwide) Factoids](english--worldwide--factoids.md)
-   [Anglais (États-Unis) Factoids](english--united-states--factoids.md)
-   [Français Factoids](french-factoids.md)
-   [Factoids allemand](german-factoids.md)
-   [Espagnol Factoids](spanish-factoids.md)

 

