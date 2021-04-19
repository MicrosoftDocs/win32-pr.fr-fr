---
description: Décrit le processus de création d’une application WSDAPI à l’aide de WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Utilisation de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545822"
---
# <a name="using-wsdcodegen"></a><span data-ttu-id="8907e-103">Utilisation de WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="8907e-103">Using WsdCodeGen</span></span>

<span data-ttu-id="8907e-104">**Pour générer une application WSDAPI à l’aide de WsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="8907e-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="8907e-105">Définissez le contrat fonctionnel pour l’hôte d’appareil dans un fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="8907e-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="8907e-106">Générez un fichier de configuration à l’aide de WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="8907e-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="8907e-107">Pour plus d’informations, consultez [fichier de configuration WsdCodeGen](wsdcodegen-configuration-file.md) et syntaxe de la [ligne de commande WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8907e-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="8907e-108">Ouvrez le fichier de configuration généré, puis modifiez le fichier en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8907e-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="8907e-109">Si vous générez une application cliente, peu ou aucune modification n’est requise.</span><span class="sxs-lookup"><span data-stu-id="8907e-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="8907e-110">Si vous générez une application hôte, modifiez les éléments de configuration spécifiques à l’utilisateur (tels que [**fabricant**](manufacturer.md) et [**modelname**](modelname.md)).</span><span class="sxs-lookup"><span data-stu-id="8907e-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="8907e-111">Générez le code à l’aide de WsdCodeGen, en fournissant le fichier de configuration en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="8907e-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="8907e-112">Pour plus d’informations, consultez Syntaxe de la [ligne de commande WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8907e-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="8907e-113">Utilisez le code généré pour générer un client, un hôte, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8907e-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="8907e-114">Le SDK Windows comprend des exemples de fichiers WSDL, des fichiers de configuration WsdCodeGen et du code généré.</span><span class="sxs-lookup"><span data-stu-id="8907e-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="8907e-115">Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8907e-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8907e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8907e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8907e-117">Exemples WSDAPI</span><span class="sxs-lookup"><span data-stu-id="8907e-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



