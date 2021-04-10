---
title: Architecture du gestionnaire
description: Architecture du gestionnaire
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029312"
---
# <a name="handler-architecture"></a><span data-ttu-id="8f73a-103">Architecture du gestionnaire</span><span class="sxs-lookup"><span data-stu-id="8f73a-103">Handler Architecture</span></span>

<span data-ttu-id="8f73a-104">La fonction interne d’un fichier ou d’un gestionnaire de flux est définie par le gestionnaire lui-même.</span><span class="sxs-lookup"><span data-stu-id="8f73a-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="8f73a-105">Pour une application, un gestionnaire de fichiers apparaît généralement sous la forme d’un module permettant de lire et d’écrire des fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="8f73a-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="8f73a-106">De même, un gestionnaire de flux apparaît en tant que module pour lire et écrire un type spécifique de flux de données.</span><span class="sxs-lookup"><span data-stu-id="8f73a-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="8f73a-107">L’interface de flux cohérent rend non importante la source et la destination du flux pour l’application qui utilise le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="8f73a-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="8f73a-108">Un gestionnaire de fichiers permet d’accéder à une source de données composée d’un ou de plusieurs flux de données.</span><span class="sxs-lookup"><span data-stu-id="8f73a-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="8f73a-109">Les gestionnaires de fichiers fournissent généralement un accès aux fichiers de disque contenant un ou plusieurs flux de données, et les fonctions internes du gestionnaire de fichiers lisent et écrivent les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="8f73a-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="8f73a-110">Toutefois, les gestionnaires de fichiers peuvent fonctionner avec n’importe quelle source de données, par exemple un canal de transmission numérique contenant plusieurs flux de données mélangés.</span><span class="sxs-lookup"><span data-stu-id="8f73a-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="8f73a-111">En revanche, un gestionnaire de flux traite un type de données et apparaît comme un flux de données pour une application.</span><span class="sxs-lookup"><span data-stu-id="8f73a-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="8f73a-112">Un gestionnaire de flux peut fournir des données qu’il fabrique ou peut récupérer des données à partir d’un fichier ou d’une source externe.</span><span class="sxs-lookup"><span data-stu-id="8f73a-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="8f73a-113">Il fournit ses données dans un format que votre application peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="8f73a-113">It supplies its data in a format that your application can use.</span></span>

 

 




