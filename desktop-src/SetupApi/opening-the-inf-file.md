---
description: Vous devez utiliser la fonction SetupOpenInfFile pour ouvrir le fichier INF avant de pouvoir récupérer des informations à partir de celui-ci ou y ajouter d’autres fichiers INF.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Ouverture du fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865718"
---
# <a name="opening-the-inf-file"></a>Ouverture du fichier INF

Vous devez utiliser la fonction [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) pour ouvrir le fichier INF avant de pouvoir récupérer des informations à partir de celui-ci ou y ajouter d’autres fichiers INF.

L’exemple suivant ouvre un fichier INF à l’aide de [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) et retourne un descripteur, MyInf, au fichier INF ouvert. Le paramètre *InfClass* de **SetupOpenInfFile** est spécifié comme **null** pour indiquer que la classe du fichier INF doit être ignorée.


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



Après l’ouverture d’un fichier INF, vous pouvez appeler la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) pour ajouter un fichier au fichier INF ouvert. Pour ajouter plusieurs fichiers, répétez ce processus. Si vous appelez la fonction **SetupOpenAppendInfFile** et que le nom de fichier qui lui est transmis est **null**, la fonction recherchera la section version du fichier INF ouvert (ainsi que tous les fichiers INF ajoutés) pour une clé LayoutFile. Si la fonction trouve une clé, elle ajoute le fichier spécifié par cette clé (généralement la disposition. INF). Lorsque plusieurs fichiers INF ont été combinés, **SetupOpenAppendInfFile** commence par le dernier fichier INF ajouté lors de la recherche d’une section de version.

 

 



