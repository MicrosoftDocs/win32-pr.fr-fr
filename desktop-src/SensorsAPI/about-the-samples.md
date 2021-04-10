---
description: Le SDK Windows contient des exemples de code et des outils utiles pour vous aider à comprendre et à utiliser le capteur Windows et la plateforme d’emplacement, ainsi que les API associées.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: À propos des exemples et des outils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867618"
---
# <a name="about-the-samples-and-tools"></a><span data-ttu-id="e943f-103">À propos des exemples et des outils</span><span class="sxs-lookup"><span data-stu-id="e943f-103">About the Samples and Tools</span></span>

<span data-ttu-id="e943f-104">Le SDK Windows contient des exemples de code et des outils utiles pour vous aider à comprendre et à utiliser le capteur Windows et la plateforme d’emplacement, ainsi que les API associées.</span><span class="sxs-lookup"><span data-stu-id="e943f-104">The Windows SDK includes useful code samples and tools to help you understand and use the Windows Sensor and Location platform and related APIs.</span></span>

## <a name="samples"></a><span data-ttu-id="e943f-105">Exemples</span><span class="sxs-lookup"><span data-stu-id="e943f-105">Samples</span></span>

<span data-ttu-id="e943f-106">Le SDK Windows comprend les exemples d’API de capteur suivants.</span><span class="sxs-lookup"><span data-stu-id="e943f-106">The Windows SDK includes the following Sensor API samples.</span></span> <span data-ttu-id="e943f-107">Vous trouverez les exemples d’API de capteur dans le dossier nommé \\ Samples \\ WinUI \\ sensors, où vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="e943f-107">You can find the Sensor API samples in the folder named \\Samples\\winui\\Sensors, where you installed the Windows SDK.</span></span> <span data-ttu-id="e943f-108">Par exemple, si vous avez installé le SDK Windows sur le lecteur C, vous trouverez les exemples dans le dossier suivant : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ WinUI \\ sensors.</span><span class="sxs-lookup"><span data-stu-id="e943f-108">For example, if you installed the Windows SDK on drive C, you would find the samples in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\winui\\Sensors.</span></span>



| <span data-ttu-id="e943f-109">Nom d’exemple</span><span class="sxs-lookup"><span data-stu-id="e943f-109">Sample name</span></span>       | <span data-ttu-id="e943f-110">Description</span><span class="sxs-lookup"><span data-stu-id="e943f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e943f-111">AmbientLightAware</span><span class="sxs-lookup"><span data-stu-id="e943f-111">AmbientLightAware</span></span> | <span data-ttu-id="e943f-112">Cet exemple MFC montre comment utiliser l’API de capteur en lisant les données des capteurs de lumière ambiante sur l’ordinateur et en modifiant la taille du texte en fonction des conditions d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="e943f-112">This MFC sample shows how to use the Sensor API by reading data from ambient light sensors on the computer and changing text size according to the lighting conditions.</span></span> <span data-ttu-id="e943f-113">Vous pouvez voir le code qui montre comment gérer des événements et comment demander des autorisations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e943f-113">You can see code that shows how to manage events and how to request user permissions.</span></span> <span data-ttu-id="e943f-114">Vous pouvez également voir un exemple de gestion de l’interface utilisateur en fonction de différentes conditions d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="e943f-114">You can also see an example of how to manage the user interface based on varying lighting conditions.</span></span> <span data-ttu-id="e943f-115">Pour plus d’informations, consultez [création d' Light-Aware interfaces utilisateur](creating-light-aware-user-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e943f-115">For more information, see [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).</span></span><br/> <span data-ttu-id="e943f-116">Vous devez avoir installé Visual Studio 2008 pour générer cet exemple.</span><span class="sxs-lookup"><span data-stu-id="e943f-116">You must have Visual Studio 2008 installed to build this sample.</span></span><br/> |



 

<span data-ttu-id="e943f-117">Pour plus d’informations, consultez le fichier nommé ReadMe.txt inclus avec l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e943f-117">For more information, see the file named ReadMe.txt that is included with the sample.</span></span>

<span data-ttu-id="e943f-118">Vous pouvez également télécharger l’exemple AmbientLightAware à partir de la Galerie de code.</span><span class="sxs-lookup"><span data-stu-id="e943f-118">You can also download the AmbientLightAware sample from Code Gallery.</span></span> <span data-ttu-id="e943f-119">Pour plus d’informations, consultez la page de téléchargement de la prise en charge de la [lumière ambiante](/samples/browse/?redirectedfrom=MSDN-samples) .</span><span class="sxs-lookup"><span data-stu-id="e943f-119">For more information, see the [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) download page.</span></span>

## <a name="tools"></a><span data-ttu-id="e943f-120">Outils</span><span class="sxs-lookup"><span data-stu-id="e943f-120">Tools</span></span>

<span data-ttu-id="e943f-121">Le SDK Windows comprend un capteur de lumière virtuelle que vous pouvez utiliser pour simuler un appareil de capteur de lumière matériel.</span><span class="sxs-lookup"><span data-stu-id="e943f-121">The Windows SDK includes a virtual light sensor that you can use to simulate a hardware-based light sensor device.</span></span> <span data-ttu-id="e943f-122">Vous pouvez utiliser cet outil pour fournir des données à l’exemple AmbientLightAware pour voir comment le code de l’exemple fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e943f-122">You can use this tool to provide data to the AmbientLightAware sample to see how the code in the sample works.</span></span>

<span data-ttu-id="e943f-123">Le tableau suivant décrit les fichiers que vous devez utiliser pour exécuter le capteur de lumière virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e943f-123">The following table describes the files you must use to run the virtual light sensor.</span></span> <span data-ttu-id="e943f-124">Ces fichiers se trouvent dans le dossier nommé bin, dans lequel vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="e943f-124">You can find these files in the folder named Bin, where you installed the Windows SDK.</span></span> <span data-ttu-id="e943f-125">Par exemple, si vous avez installé le SDK Windows sur le lecteur C sur un ordinateur 32 bits, vous trouverez les fichiers de capteur de lumière virtuelle dans le dossier suivant : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="e943f-125">For example, if you installed the Windows SDK on drive C on a 32-bit computer, you would find the virtual light sensor files in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Bin.</span></span> <span data-ttu-id="e943f-126">Sur les ordinateurs 64 bits, vous devez utiliser la version 64 bits de l’outil.</span><span class="sxs-lookup"><span data-stu-id="e943f-126">On 64-bit computers, you must use the 64-bit version of the tool.</span></span> <span data-ttu-id="e943f-127">Dans le SDK Windows, les outils 64 bits se trouvent dans le sous-dossier nommé x64.</span><span class="sxs-lookup"><span data-stu-id="e943f-127">In the Windows SDK, 64-bit tools are located in the subfolder named x64.</span></span>



| <span data-ttu-id="e943f-128">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="e943f-128">File name</span></span>                    | <span data-ttu-id="e943f-129">Description</span><span class="sxs-lookup"><span data-stu-id="e943f-129">Description</span></span>                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e943f-130">VirtualLightSensor.exe</span><span class="sxs-lookup"><span data-stu-id="e943f-130">VirtualLightSensor.exe</span></span>       | <span data-ttu-id="e943f-131">Ce programme fournit un contrôle Slider qui vous permet de modifier le niveau des données de lumière que le capteur virtuel signale.</span><span class="sxs-lookup"><span data-stu-id="e943f-131">This program provides a slider control that enables you to change the level of the light data that the virtual sensor reports.</span></span> |
| <span data-ttu-id="e943f-132">VirtualLightSensorDriver.dll</span><span class="sxs-lookup"><span data-stu-id="e943f-132">VirtualLightSensorDriver.dll</span></span> | <span data-ttu-id="e943f-133">Pilote de capteur logique qui simule un capteur de lumière.</span><span class="sxs-lookup"><span data-stu-id="e943f-133">The logical sensor driver that simulates a light sensor.</span></span>                                                                       |
| <span data-ttu-id="e943f-134">VirtualLightSensorDriver. inf</span><span class="sxs-lookup"><span data-stu-id="e943f-134">VirtualLightSensorDriver.inf</span></span> | <span data-ttu-id="e943f-135">Fichier INF du pilote de capteur de lumière virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e943f-135">The INF file for the virtual light sensor driver.</span></span>                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a><span data-ttu-id="e943f-136">Installation du capteur de lumière virtuelle</span><span class="sxs-lookup"><span data-stu-id="e943f-136">Installing the Virtual Light Sensor</span></span>

<span data-ttu-id="e943f-137">Avant d’utiliser l’application de capteur d’éclairage virtuel, vous devez installer le pilote de capteur logique.</span><span class="sxs-lookup"><span data-stu-id="e943f-137">Before you use the virtual light sensor application, you must install the logical sensor driver.</span></span> <span data-ttu-id="e943f-138">Suivez ces étapes :</span><span class="sxs-lookup"><span data-stu-id="e943f-138">Follow these steps:</span></span>

1.  <span data-ttu-id="e943f-139">Ouvrez une fenêtre de commande en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e943f-139">Open a command window as an administrator.</span></span>
2.  <span data-ttu-id="e943f-140">Accédez au dossier SDK Windows bin.</span><span class="sxs-lookup"><span data-stu-id="e943f-140">Change to the Windows SDK Bin folder.</span></span>
3.  <span data-ttu-id="e943f-141">Tapez **PnPUtil-a VirtualLightSensorDriver. inf**.</span><span class="sxs-lookup"><span data-stu-id="e943f-141">Type **pnputil -a VirtualLightSensorDriver.inf**.</span></span>
4.  <span data-ttu-id="e943f-142">Quand vous y êtes invité, cliquez sur **installer ce pilote logiciel quand même**.</span><span class="sxs-lookup"><span data-stu-id="e943f-142">When prompted, click **Install this driver software anyway**.</span></span>
5.  <span data-ttu-id="e943f-143">Attendez que la fenêtre de commande signale que le pilote a été correctement installé.</span><span class="sxs-lookup"><span data-stu-id="e943f-143">Wait for the command window to report that the driver was successfully installed.</span></span>

### <a name="running-the-virtual-light-sensor"></a><span data-ttu-id="e943f-144">Exécution du capteur de lumière virtuelle</span><span class="sxs-lookup"><span data-stu-id="e943f-144">Running the Virtual Light Sensor</span></span>

<span data-ttu-id="e943f-145">Pour exécuter le capteur de lumière virtuelle, il vous suffit de double-cliquer sur le fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="e943f-145">To run the virtual light sensor, simply double-click the .exe file.</span></span> <span data-ttu-id="e943f-146">Veillez à activer le capteur quand vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="e943f-146">Be sure to enable the sensor, when prompted.</span></span>

<span data-ttu-id="e943f-147">Lorsque vous exécutez le programme, vous pouvez remarquer qu’il y a un délai avant que le capteur ne soit disponible.</span><span class="sxs-lookup"><span data-stu-id="e943f-147">When you run the program, you may notice that there is a delay before the sensor becomes available.</span></span> <span data-ttu-id="e943f-148">L’interface utilisateur du capteur de lumière virtuelle affiche le message « en attente » dans la barre de titre, tandis que le gestionnaire de capteurs logiques crée un nœud de périphérique pour le capteur logique.</span><span class="sxs-lookup"><span data-stu-id="e943f-148">The virtual light sensor user interface will display the message "Waiting" in the title bar while the logical sensor manager creates a device node for the logical sensor.</span></span> <span data-ttu-id="e943f-149">Une fois le message en attente supprimé, vous pouvez utiliser le curseur pour définir le niveau de sortie Lux pour le capteur de lumière virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e943f-149">After the waiting message goes away, you can use the slider to set the lux output level for the virtual light sensor.</span></span>

<span data-ttu-id="e943f-150">L’illustration suivante montre l’interface utilisateur du capteur d’éclairage virtuel dans son état prêt.</span><span class="sxs-lookup"><span data-stu-id="e943f-150">The following image shows the virtual light sensor user interface in its ready state.</span></span>

![interface utilisateur du capteur d’éclairage virtuel](images/virtuallightsensor.png)

## <a name="related-topics"></a><span data-ttu-id="e943f-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e943f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e943f-153">À propos des capteurs logiques</span><span class="sxs-lookup"><span data-stu-id="e943f-153">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> <dt>

[<span data-ttu-id="e943f-154">**catégorie de capteur \_ \_ Light**</span><span class="sxs-lookup"><span data-stu-id="e943f-154">**SENSOR\_CATEGORY\_LIGHT**</span></span>](sensor-category-light.md)
</dt> </dl>

 

