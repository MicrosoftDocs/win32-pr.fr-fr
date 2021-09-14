---
title: Présentation de StoClien
description: L’exemple StoClien montre comment le client utilise le stockage structuré et comment il dirige un composant serveur pour utiliser ce stockage.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Présentation de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee37f6f84cf981bda637abbd96ff8e8f0314d8ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013547"
---
# <a name="stoclien-overview"></a>Présentation de StoClien

## <a name="purpose"></a>Objectif

L’objectif principal de l’exemple [StoClien](structured-storage-client-sample--stoclien-.md) est la manière dont le client utilise le stockage structuré et comment il demande à un composant serveur d’utiliser ce stockage. L’exemple StoClien illustre un modèle de programmation de services de stockage structuré.

## <a name="functionality"></a>Fonctionnalité

La fonctionnalité [StoClien](structured-storage-client-sample--stoclien-.md) est similaire aux exemples « Scribble » dans certaines versions de Microsoft Visual C++. La différence entre l’exemple StoClien et l’exemple [StoServe](structured-storage-server-sample--stoserve-.md) est une architecture interne basée sur la technologie com. Une distinction architecturale claire est conservée entre le client COM et le serveur COM.

[StoClien](structured-storage-client-sample--stoclien-.md) charge et enregistre ses dessins dans le stockage structuré des fichiers composés com.

L’exemple [StoClien](structured-storage-client-sample--stoclien-.md) crée et utilise l’objet com de coalimentation connectable fourni en tant que \_ composant CLSID DllPaper sur le serveur [StoServe](structured-storage-server-sample--stoserve-.md) . Le client StoClien crée un objet coimprimé et le contrôle par le biais de l’interface IPaper exposée par l’objet. StoClien obtient des données de dessin de l’utilisateur et les représente sous forme graphique dans une fenêtre qu’il gère. StoClien utilise l’interface IPaper du copapier pour enregistrer les données de dessin dans un colivre et pour diriger les opérations de stockage de fichiers sur ces données.

Un objet COM de type « codocument » encapsule uniquement le stockage serveur des données du papier de dessin : aucun comportement de l’interface graphique utilisateur n’est fourni côté serveur. Tout le comportement de l’interface utilisateur graphique est isolé dans le client. Les fonctionnalités de stockage et de gestion des données des objets de codocumentation sont disponibles uniquement via une interface COM personnalisée, IPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) coopère avec le copapier pour charger et enregistrer les données de dessin du plan. StoClien obtient une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour l’objet de stockage dans un fichier composé. Dans ses opérations de chargement et d’enregistrement, StoClien transmet un pointeur vers l’interface **IStorage** au contours du serveur. Le colivre utilise le **IStorage** fourni pour créer des flux dans le stockage. Le colivre peut ensuite utiliser l’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) standard pour lire et écrire les données de dessin qu’il gère.

Le colivre gère uniquement les données de dessin ; Il n’effectue aucune action de l’interface utilisateur graphique. [StoClien](structured-storage-client-sample--stoclien-.md) fournit l’interface graphique utilisateur de l’application de dessin. Il encapsule ce dans un objet C++ central CGuiPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) implémente également l’interface IPaperSink personnalisée dans un objet com COPaperSink et connecte cette interface à un point de connexion approprié dans l’objet de codocumentation de serveur. Le colivre utilise l’interface IPaperSink connectée pour renvoyer des notifications à StoClien. L’interface graphique utilisateur normale redessinant les données de dessin du plan est effectuée dans StoClien à l’aide de la technologie d’objets connectable du colivre.

[StoClien](structured-storage-client-sample--stoclien-.md) est une application que vous pouvez exécuter directement de manière normale ou à partir de la fenêtre d’invite de commandes. StoClien accepte un paramètre de nom de fichier facultatif sur la ligne de commande.

Dans l’exemple suivant, Drawing. PAP est un fichier composé contenant le stockage structuré compatible DllPaper des données de dessin. Si aucun paramètre de nom de fichier de ligne de commande n’est spécifié, [StoClien](structured-storage-client-sample--stoclien-.md) utilise le nom de fichier par défaut StoClien. PAP et tente de l’ouvrir dans le même répertoire que le Stoclien.exe en cours d’exécution.

**StoClien c : \\ dessins \\ dessin. PAP**

## <a name="support-information"></a>Informations de support

Pour plus d’informations, des descriptions fonctionnelles et un didacticiel de code pour [StoClien](structured-storage-client-sample--stoclien-.md), consultez la section relative à la visite guidée du code dans Stoclien.htm. Pour plus d’informations sur l’opération utilisateur externe de StoClien, consultez les sections utilisation et opération dans Stoclien.htm. Pour lire Stoclient.htm, exécutez Tutorial.exe dans le répertoire principal du didacticiel, puis cliquez sur la leçon StoClien dans le tableau des leçons. vous pouvez également cliquer sur Stoclien.htm après avoir localisé le répertoire principal du didacticiel dans Windows Explorer. Pour plus d’informations sur le fonctionnement de [**StoServe**](structured-storage-server-sample--stoserve-.md) et sur l’exposition de ses services à StoClien, consultez Stoserve.htm dans le répertoire principal du didacticiel. N’oubliez pas que vous devez générer le Stoserve.dll avant de générer StoClien. Le makefile pour [**StoServe**](structured-storage-server-sample--stoserve-.md) inscrit ce serveur dans le registre système. vous devez donc générer [**StoServe**](structured-storage-server-sample--stoserve-.md) avant d’exécuter StoClien.

Pour plus d’informations sur la configuration d’un système pour générer et tester les exemples de code de cette série de didacticiels COM, consultez [Comment générer des exemples](how-to-build-samples.md). Le Makefile fourni (MAKEFILE) est compatible avec Microsoft NMAKE. Pour créer une version Debug, émettez la commande NMAKE dans la fenêtre d’invite de commandes.

Pour plus de commodité, un fichier projet est fourni pour chaque exemple pour une utilisation dans Microsoft Visual Studio. pour charger le projet de l’exemple [StoClien](structured-storage-client-sample--stoclien-.md) , exécutez Visual Studio à l’invite de commandes dans le répertoire de l’exemple comme suit :

MSDEV STOCLIEN. DSP

vous pouvez également double-cliquer sur le fichier Stoclient. dsp dans Windows Explorer pour charger un exemple de projet dans Visual Studio. dans Visual Studio, vous pouvez parcourir les classes C++ de l’exemple de source et effectuer généralement les autres opérations de modification-compilation-débogage. n’oubliez pas que, dans le cadre du kit de développement logiciel (SDK) du serveur, la compilation de ces exemples à partir de Visual Studio requiert le paramètre approprié des chemins d’accès aux répertoires dans Visual Studio. Pour plus d’informations, consultez [Comment générer des exemples](how-to-build-samples.md).

## <a name="remarks"></a>Notes

L’exemple de client et d’autres exemples associés doivent être compilés avant que vous puissiez exécuter le client. Pour plus d’informations sur la création des exemples, consultez [Comment générer des exemples](how-to-build-samples.md). Si vous avez généré les exemples appropriés, Stoclien.exe est l’exécutable client à exécuter pour cet exemple.

L’application Stoclien.exe fournit l’interface utilisateur de ce didacticiel. Elle exerce le Stoserve.dll associé, mais indépendant, pour démontrer l’utilisation par le client et le serveur du stockage structuré COM dans des fichiers composés.

 

 




