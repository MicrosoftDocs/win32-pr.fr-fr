---
title: Créer et exécuter un exemple StoClien
description: StoClien travaille en collaboration avec un objet codocument dans un serveur COM pour obtenir un stockage persistant des dessins dans les fichiers composés COM.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Créer et exécuter un exemple StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3d9526e81fc3fb2d6a0cfb03e8943ccf68688096588122da87861d8c88e531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663459"
---
# <a name="create-and-run-stoclien-sample"></a>Créer et exécuter un exemple StoClien

**StoClien** travaille en collaboration avec un objet codocument dans un serveur com pour obtenir un stockage persistant des dessins dans les fichiers composés com. Pour plus d’informations sur l’utilisation par le biais de flux de données dans le fichier composé fourni au **StoClien**, consultez l’exemple [**StoServe**](structured-storage-server-sample--stoserve-.md) et STOSERVE.HTM. La construction du copapier et son interface IPaper sont également abordées dans l’exemple **StoServe** .

## <a name="code-tour"></a>Visite guidée du code

Les principales rubriques traitées dans cette présentation du code sont les suivantes :

-   Comment **CGuiPaper** encapsule le comportement de l’interface graphique du papier de dessin électronique de **StoClien**
-   Comment **StoClien** capture et affiche l’activité de dessin interactif
-   Comment l’objet **CGuiPaper** utilise le codocument pour enregistrer les données de dessin
-   Utilisation d’une connexion IPaperSink pour le redessin
-   Comment les méthodes **Load** et **Save** de CPapFile utilisent le stockage structuré dans des fichiers composés

Comme la classe **CGuiBall** utilisée dans les exemples FRECLIEN et CONCLIEN a encapsulé le comportement d’une balle rebondissante, **StoClien** utilise une classe **CGuiPaper** C++ pour encapsuler les données et le comportement de l’interface graphique utilisateur du papier de dessin électronique.

Le tableau suivant répertorie les fichiers pertinents pour l’exemple **StoClien** .



| Fichiers        | Description                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Brève description de l’exemple.                                                                                                        |
| ADOPTE     | Makefile générique pour la génération de l’exemple de code.                                                                               |
| STOCLIEN. Manutention   | Fichier include pour l’application **StoClien** . Contient des déclarations de classe, des prototypes de fonction et des identificateurs de ressource.   |
| STOCLIEN. COTISATIONS | Fichier d’implémentation principal pour STOCLIEN.EXE. A une implémentation de WinMain et CMainWindow, ainsi que la distribution du menu principal. |
| STOCLIEN. Release  | Fichier de définition de ressource d’application.                                                                                        |
| STOCLIEN. ICO | Ressource icône d’application.                                                                                                   |
| STOCLIEN. Protocole | Fichier de dessin papier par défaut pour l’application.                                                                                |
| Crayon. Tabs   | Image de crayon pour le curseur de la fenêtre cliente.                                                                                     |
| Puits. Manutention       | Déclaration de classe pour la classe d’objets COM COPaperSink.                                                                      |
| Puits. COTISATIONS     | Fichier d’implémentation pour la classe d’objets COM COPaperSink.                                                                        |
| PAPFILE. Manutention    | Déclaration de classe pour la classe C++ **CPapFile** .                                                                            |
| PAPFILE. COTISATIONS  | Fichier d’implémentation pour la classe C++ **CPapFile** .                                                                              |
| GUIPAPER. Manutention   | Déclaration de classe pour la classe C++ **CGuiPaper** .                                                                           |
| GUIPAPER. COTISATIONS | Fichier d’implémentation pour la classe C++ **CGuiPaper** .                                                                             |
| STOCLIEN. DSP | Microsoft Visual Studio Project fichier.                                                                                            |



 

## <a name="compound-files"></a>Fichiers composés

**StoClien** s’appuie sur le codocument pour enregistrer les données de dessin. Il s’appuie également sur le copapier pour stocker les données dans un fichier composé. Toutefois, dans une division classique du travail entre le client et le serveur COM, **StoClien** partage une partie de la responsabilité pour le stockage de fichiers. Cette division de main-d’œuvre est importante dans les applications COM où le client est un conteneur et le serveur est un objet incorporé. Dans cette organisation, le client est responsable de la création ou de l’ouverture d’un fichier de stockage structuré, tandis que l’objet serveur est chargé d’utiliser ce stockage pour ses propres fonctions de stockage de données. Cela peut impliquer l’objet serveur qui crée des sous-stockages dans le stockage qui lui est donné. Il implique généralement l’objet serveur qui crée des objets de flux dans le stockage. L’utilisation par le biais de flux de stockage est détaillée dans l’exemple **StoClien** .

L’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) est utilisée par l’objet client et le serveur pour effectuer des opérations sur les fichiers. l’implémentation des fichiers composés de l’architecture Stockage structurée est utilisée. Les fonctions de service standard sont utilisées pour les opérations sur les fichiers composés. Par exemple, la fonction [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) crée initialement un fichier composé et transmet un pointeur **IStorage** qui peut être utilisé pour manipuler le fichier. Cette fonction particulière est appelée dans **StoClien**. L’interface **IStorage** qu’elle obtient est transmise en tant que paramètre au codocument pour son utilisation. L’objet codocument ne crée pas ou n’ouvre pas les fichiers composés de manière autonome : il utilise les interfaces **IStorage** et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pour travailler dans des fichiers composés qui lui sont attribués.

Ces interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ne sont pas implémentées dans **StoClien** ou **StoServe**. Elles sont implémentées dans les bibliothèques COM. Lorsqu’un pointeur vers l’une de ces interfaces est obtenu, leurs méthodes sont essentiellement utilisées comme un ensemble de services pour opérer sur un fichier composé.

 

 




