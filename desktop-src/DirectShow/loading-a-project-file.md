---
description: Chargement d’un fichier projet
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Chargement d’un fichier projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200739"
---
# <a name="loading-a-project-file"></a>Chargement d’un fichier projet

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Pour charger un fichier projet, vous avez besoin de deux composants : l’analyseur XML et une chronologie vide. L’analyseur XML lit un fichier de projet XML et crée chaque objet défini dans le fichier. Elle insère ensuite les objets dans la chronologie et définit tous les attributs de la chronologie, tels que la fréquence d’images par défaut. L’exemple de code suivant charge un fichier.


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



L’analyseur expose l’interface [**IXml2Dex**](ixml2dex.md) , qui contient des méthodes pour le chargement et l’enregistrement des fichiers projet. La chronologie expose l’interface [**IAMTimeline**](iamtimeline.md) , qui contient des méthodes pour manipuler la chronologie et créer des objets Timeline. Appelez la fonction **CoCreateInstance** pour créer chaque composant, comme indiqué. N’oubliez pas qu’en créant une nouvelle instance, vous incrémentez le décompte de références sur l’interface. Pour éviter les fuites de mémoire, libérez toujours une interface quand vous le souhaitez. Dans cet exemple, le pointeur vers **IXml2Dex** n’est pas nécessaire pour d’autres choses. vous pouvez donc libérer l’interface. Le pointeur vers **IAMTimeline** est toujours nécessaire pour afficher un aperçu de la chronologie.

La méthode [**IXml2Dex :: ReadXMLFile**](ixml2dex-readxmlfile.md) lit le fichier spécifié et remplit la chronologie avec les objets définis dans le fichier. Le nom de fichier est spécifié à l’aide d’une valeur **BSTR** . Pour raccourcir l’exemple, le nom de fichier dans l’exemple est donné sous la forme d’une chaîne littérale. Normalement, vous l’obtenez à partir d’une boîte de dialogue Ouvrir un fichier ou d’un nom similaire.

Si la méthode **ReadXml** réussit, elle retourne un code de réussite. Sinon, elle retourne un code d’erreur tel que VFW \_ E \_ format de fichier non valide \_ \_ . Vérifiez toujours la valeur de retour, afin de gérer les conditions d’erreur normalement. Là encore, par souci de concision, l’exemple de code ne vérifie pas les erreurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chargement et affichage de l’aperçu d’un projet](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



