---
description: L’encodage fait référence au processus de conversion de médias numériques d’un format dans un autre. Par exemple, la conversion de son MP3 au format Windows Media Audio comme défini par la spécification ASF (Advanced Systems Format).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Didacticiel : 1-passer l’encodage Windows Media'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761461"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="e8fc2-104">Didacticiel : 1-passer l’encodage Windows Media</span><span class="sxs-lookup"><span data-stu-id="e8fc2-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="e8fc2-105">L’encodage fait référence au processus de conversion de médias numériques d’un format dans un autre.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="e8fc2-106">Par exemple, la conversion de son MP3 au format Windows Media Audio comme défini par la spécification ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="e8fc2-107">**Remarque**  La spécification ASF définit un type de conteneur pour le fichier de sortie (. WMA ou. wmv) qui peut contenir des données multimédias dans n’importe quel format, compressé ou non compressé.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="e8fc2-108">Par exemple, un conteneur ASF comme un fichier. WMA peut contenir des données multimédias au format MP3.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="e8fc2-109">Le processus d’encodage convertit le format réel des données contenues dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="e8fc2-110">Ce didacticiel montre l’encodage d’une source d’entrée de contenu clair (non protégée par DRM) dans le contenu Windows Media et l’écriture de données dans un nouveau fichier ASF (. WM \* ) à l’aide de composants ASF de couche de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="e8fc2-111">Ces composants seront utilisés pour générer une topologie d’encodage partielle, qui sera contrôlée par une instance de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="e8fc2-112">Dans ce didacticiel, vous allez créer une application console qui prend les noms de fichiers d’entrée et de sortie, et le mode d’encodage comme arguments.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="e8fc2-113">Le fichier d’entrée peut être dans un format compressé ou non compressé.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="e8fc2-114">Les modes d’encodage valides sont « CBR » (vitesse binaire constante) ou « VBR » (vitesse de transmission variable).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="e8fc2-115">L’application crée une source de média pour représenter la source spécifiée par le nom de fichier d’entrée, et le récepteur de fichiers ASF pour archiver le contenu encodé du fichier source dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="e8fc2-116">Pour simplifier l’implémentation du scénario, le fichier de sortie n’aura qu’un seul flux audio et un seul flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="e8fc2-117">L’application insère le codec Windows Media Audio 9,1 Professional pour la conversion de format de flux audio et le codec Windows Media Video 9 pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="e8fc2-118">Pour un encodage à taux binaire constant, avant le début de la session d’encodage, l’encodeur doit connaître la vitesse de transmission cible qu’il doit atteindre.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="e8fc2-119">Dans ce didacticiel, pour le mode « CBR », l’application utilise la vitesse de transmission disponible avec le premier type de média de sortie récupéré à partir de l’encodeur pendant la négociation de type de média comme vitesse de transmission cible.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="e8fc2-120">Pour l’encodage à taux binaire variable, ce didacticiel montre l’encodage avec une vitesse de transmission variable en définissant un niveau de qualité.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="e8fc2-121">Les flux audio sont encodés au niveau de qualité 98 et les flux vidéo au niveau de qualité 95.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="e8fc2-122">La procédure suivante résume les étapes d’encodage du contenu Windows Media dans un conteneur ASF à l’aide d’un mode d’encodage à passage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="e8fc2-123">Créer une source de média pour le spécifié à l’aide du programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="e8fc2-124">Énumérer les flux dans la source du média.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="e8fc2-125">Créez le récepteur de média ASF et ajoutez des récepteurs de flux en fonction des flux de la source du média qui doivent être encodés.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="e8fc2-126">Configurez le récepteur multimédia avec les propriétés d’encodage requises.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="e8fc2-127">Créez les encodeurs Windows Media pour les flux dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="e8fc2-128">Configurez les encodeurs avec les propriétés définies sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="e8fc2-129">Générez une topologie d’encodage partielle.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="e8fc2-130">Instanciez la session multimédia et définissez la topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="e8fc2-131">Démarrez la session d’encodage en contrôlant la session multimédia et en obtenant tous les événements pertinents à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="e8fc2-132">Pour l’encodage VBR, récupérez les valeurs de propriété d’encodage de l’encodeur et définissez-les sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="e8fc2-133">Fermez et arrêtez la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="e8fc2-134">Ce didacticiel contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="e8fc2-135">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="e8fc2-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e8fc2-136">Configurer le projet</span><span class="sxs-lookup"><span data-stu-id="e8fc2-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="e8fc2-137">Créer la source du média</span><span class="sxs-lookup"><span data-stu-id="e8fc2-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="e8fc2-138">Créer le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="e8fc2-139">Créer l’objet de profil ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="e8fc2-140">Créer un type de média audio compressé</span><span class="sxs-lookup"><span data-stu-id="e8fc2-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="e8fc2-141">Créer un type de média vidéo compressé</span><span class="sxs-lookup"><span data-stu-id="e8fc2-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="e8fc2-142">Créer l’objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="e8fc2-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="e8fc2-143">Créer le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="e8fc2-144">Créer la topologie d’encodage partiel</span><span class="sxs-lookup"><span data-stu-id="e8fc2-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="e8fc2-145">Créer le nœud de topologie source pour la source du média</span><span class="sxs-lookup"><span data-stu-id="e8fc2-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="e8fc2-146">Instancier les encodeurs requis et créer les nœuds de transformation</span><span class="sxs-lookup"><span data-stu-id="e8fc2-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="e8fc2-147">Créer les nœuds de topologie de sortie pour le récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="e8fc2-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="e8fc2-148">Connecter les nœuds source, de transformation et récepteur</span><span class="sxs-lookup"><span data-stu-id="e8fc2-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="e8fc2-149">Gestion de la session d’encodage</span><span class="sxs-lookup"><span data-stu-id="e8fc2-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="e8fc2-150">Mettre à jour les propriétés d’encodage dans le récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="e8fc2-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="e8fc2-151">Implémenter main</span><span class="sxs-lookup"><span data-stu-id="e8fc2-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="e8fc2-152">Tester le fichier de sortie</span><span class="sxs-lookup"><span data-stu-id="e8fc2-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="e8fc2-153">Codes d’erreur courants et conseils de débogage</span><span class="sxs-lookup"><span data-stu-id="e8fc2-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="e8fc2-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8fc2-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e8fc2-155">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e8fc2-155">Prerequisites</span></span>

<span data-ttu-id="e8fc2-156">Ce didacticiel part des principes suivants :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="e8fc2-157">Vous êtes familiarisé avec la [structure de fichiers ASF](asf-file-structure.md), les [composants ASF de couche de pipeline](pipeline-layer-asf-components.md) fournis par Media Foundation pour travailler avec des objets ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="e8fc2-158">Ces composants incluent les objets suivants :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="e8fc2-159">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="e8fc2-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="e8fc2-160">**Remarque**  Si vous effectuez une conversion (en convertissant un fichier de taux binaire plus élevé en un fichier de vitesse de transmission inférieur sans modifier les formats), vous utiliserez la [source du média ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="e8fc2-161">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="e8fc2-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="e8fc2-162">Récepteurs de média ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="e8fc2-163">Objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="e8fc2-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="e8fc2-164">Profil ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="e8fc2-165">Vous êtes familiarisé avec les encodeurs Windows Media et les différents types d’encodage, notamment le [codage à vitesse de transmission constant](constant-bit-rate-encoding.md) et l' [encodage à vitesse de transmission variable basé sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="e8fc2-166">Vous êtes familiarisé avec les opérations de l’encodeur MFT.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="e8fc2-167">En particulier, la création d’une instance de l’encodeur et la définition des types d’entrée et de sortie sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="e8fc2-168">Vous êtes familiarisé avec les objets de topologie et comment créer une topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="e8fc2-169">Pour plus d’informations sur les topologies et les nœuds de topologie, consultez [création de topologies](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="e8fc2-170">Vous êtes familiarisé avec le modèle d’événement de la [session de média](media-session.md)et les opérations de contrôle de Workflow.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="e8fc2-171">Pour plus d’informations, consultez [événements de session multimédia](media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="e8fc2-172">Configurer le projet</span><span class="sxs-lookup"><span data-stu-id="e8fc2-172">Set up the Project</span></span>

1.  <span data-ttu-id="e8fc2-173">Incluez les en-têtes suivants dans votre fichier source :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-173">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  <span data-ttu-id="e8fc2-174">Lien vers les fichiers de bibliothèque suivants :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="e8fc2-175">Déclarez la fonction [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  <span data-ttu-id="e8fc2-176">Déclarez l' \_ énumération du mode d’encodage pour définir les types d’encodage CBR et VBR.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="e8fc2-177">Définissez une constante pour la fenêtre de mémoire tampon d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="e8fc2-178">Créer la source du média</span><span class="sxs-lookup"><span data-stu-id="e8fc2-178">Create the Media Source</span></span>

<span data-ttu-id="e8fc2-179">Créez une source de média pour la source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-179">Create a media source for the input source.</span></span> <span data-ttu-id="e8fc2-180">Media Foundation fournit des sources multimédias intégrées pour différents formats de média : MP3, MP4/3GP, AVI/WAVE.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="e8fc2-181">Pour plus d’informations sur les formats pris en charge par Media Foundation, consultez [formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="e8fc2-182">Pour créer la source du média, utilisez le programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="e8fc2-183">Cet objet analyse l’URL qui a été spécifiée pour le fichier source et crée la source de média appropriée.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="e8fc2-184">Effectuez les appels suivants :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-184">Make the following calls:</span></span>

-   [<span data-ttu-id="e8fc2-185">**MFCreateSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="e8fc2-186">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="e8fc2-187">Pour plus d’informations sur ces appels, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="e8fc2-188">Si votre fichier d’entrée est au format ASF et que vous souhaitez le convertir en un fichier de vitesse de transmission différent sans modifier les formats, le solveur source crée une instance de la [source du média ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="e8fc2-189">L’exemple de code suivant montre une fonction CreateMediaSource qui crée une source de média pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="e8fc2-190">Créer le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-190">Create the ASF File Sink</span></span>

<span data-ttu-id="e8fc2-191">Créez une instance du récepteur de fichiers ASF qui archivera les données multimédias encodées dans un fichier ASF à la fin de la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="e8fc2-192">Dans ce didacticiel, vous allez créer un objet d’activation pour le récepteur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="e8fc2-193">Le récepteur de fichiers a besoin des informations suivantes pour créer les récepteurs de flux requis.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="e8fc2-194">Flux à encoder et à écrire dans le fichier final.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="e8fc2-195">Les propriétés d’encodage utilisées pour encoder le contenu multimédia, telles que, le type d’encodage, le nombre de passes d’encodage et les propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="e8fc2-196">Propriétés de fichier globales qui indiquent au récepteur multimédia s’il doit ajuster automatiquement les paramètres de compartiment perdu (vitesse de transmission et taille de mémoire tampon).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="e8fc2-197">Les informations de flux de données sont configurées dans l’objet de profil ASF et les propriétés d’encodage et globales sont définies dans une banque de propriétés gérée par l’objet ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="e8fc2-198">Pour obtenir une vue d’ensemble du récepteur de fichiers ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="e8fc2-199">Créer l’objet de profil ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="e8fc2-200">Pour que le récepteur de fichiers ASF écrive les données multimédias encodées dans un fichier ASF, le récepteur doit connaître le nombre de flux et le type de flux pour lesquels créer des récepteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="e8fc2-201">Dans ce didacticiel, vous allez extraire ces informations de la source du média et créer les flux de sortie correspondants.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="e8fc2-202">Limitez vos flux de sortie à un flux audio et à un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="e8fc2-203">Pour chaque flux sélectionné dans la source, créez un flux cible et ajoutez-le au profil.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="e8fc2-204">Pour implémenter cette étape, vous avez besoin des objets suivants.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="e8fc2-205">Profil ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="e8fc2-206">Descripteur de présentation pour la source du média</span><span class="sxs-lookup"><span data-stu-id="e8fc2-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="e8fc2-207">Descripteurs de flux pour les flux sélectionnés dans la source du média.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="e8fc2-208">Types de médias pour les flux sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="e8fc2-209">Les étapes suivantes décrivent le processus de création du profil ASF et des flux cibles.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="e8fc2-210">**Pour créer le profil ASF**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="e8fc2-211">Appelez [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) pour créer un objet de profil vide.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="e8fc2-212">Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) pour créer le descripteur de présentation pour la source de média créée à l’étape décrite dans la section « créer la source du média » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="e8fc2-213">Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) pour connaître le nombre de flux dans la source du média.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="e8fc2-214">Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour chaque flux dans la source du média, puis récupérez le descripteur de flux du flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="e8fc2-215">Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) suivi de [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) et récupérez le premier type de média pour le flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="e8fc2-216">**Remarque**   Pour éviter les appels complexes, supposez qu’il n’existe qu’un seul type de média par flux et sélectionnez le premier type de média du flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="e8fc2-217">Pour les flux complexes, vous devez énumérer chaque type de média à partir du gestionnaire de type de média et choisir le type de média que vous souhaitez Encoder.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="e8fc2-218">Appelez I [**IMFMediaType :: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) pour obtenir le type principal du flux afin de déterminer si le flux contient des données audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="e8fc2-219">En fonction du type principal du flux, créez des types de médias cibles.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="e8fc2-220">Ces types de médias contiendront les informations de format que l’encodeur utilisera pendant la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="e8fc2-221">Les sections suivantes de ce didacticiel décrivent le processus de création des types de média cible.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="e8fc2-222">Créer un type de média audio compressé</span><span class="sxs-lookup"><span data-stu-id="e8fc2-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="e8fc2-223">Créer un type de média vidéo compressé</span><span class="sxs-lookup"><span data-stu-id="e8fc2-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="e8fc2-224">Créez un flux basé sur le type de média cible, configurez le flux en fonction des exigences de l’application et ajoutez le flux au profil.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="e8fc2-225">Pour plus d’informations, consultez [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="e8fc2-226">Appelez [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) et transmettez le type de média cible pour créer le flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="e8fc2-227">La méthode récupère l’interface IMFASFStreamConfig de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="e8fc2-228">Configurez le flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-228">Configure the stream.</span></span>
        -   <span data-ttu-id="e8fc2-229">Appelez [**IMFASFStreamConfig :: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) pour assigner un nombre au flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="e8fc2-230">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="e8fc2-231">Éventuellement, configurez les paramètres de compartiment avec fuite, l’extension de charge utile et l’exclusion mutuelle sur chaque flux en appelant les méthodes [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) et les attributs de configuration de flux pertinents.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="e8fc2-232">Ajoutez les propriétés d’encodage de niveau de flux à l’aide de l’objet ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="e8fc2-233">Pour plus d’informations sur cette étape, consultez la section « créer l’objet ASF ContentInfo » dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="e8fc2-234">Appelez [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) pour ajouter le flux au profil.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="e8fc2-235">L’exemple de code suivant crée un flux audio de sortie.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-235">The following code example creates an output audio stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    <span data-ttu-id="e8fc2-236">L’exemple de code suivant crée un flux vidéo de sortie.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-236">The following code example creates an output video stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

<span data-ttu-id="e8fc2-237">L’exemple de code suivant crée des flux de sortie en fonction des flux dans la source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-237">The following code example creates output streams depending on the streams in the source.</span></span>


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="e8fc2-238">Créer un type de média audio compressé</span><span class="sxs-lookup"><span data-stu-id="e8fc2-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="e8fc2-239">Si vous souhaitez inclure un flux audio dans le fichier de sortie, créez un type audio en spécifiant les caractéristiques du type encodé en définissant les attributs requis.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="e8fc2-240">Pour vous assurer que le type audio est compatible avec l’encodeur audio Windows Media, instanciez la MFT de l’encodeur, définissez les propriétés d’encodage et récupérez un type de média en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="e8fc2-241">Obtenez le type de sortie requis en parcourant tous les types disponibles, en obtenant les attributs de chaque type de média et en sélectionnant le type le plus proche de vos spécifications.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="e8fc2-242">Dans ce didacticiel, récupérez le premier type disponible dans la liste des types de médias de sortie pris en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="e8fc2-243">**Remarque**  Pour Windows 7, Media Foundation fournit une nouvelle fonction, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , qui récupère la liste des types audio compatibles.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="e8fc2-244">Cette fonction obtient uniquement les types de médias pour l’encodage CBR.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="e8fc2-245">Un type audio complet doit avoir les attributs suivants définis :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="e8fc2-246">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="e8fc2-247">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="e8fc2-248">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="e8fc2-249">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="e8fc2-250">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="e8fc2-251">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="e8fc2-252">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="e8fc2-253">L’exemple de code suivant crée un type audio compressé en obtenant un type compatible à partir de l’encodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="e8fc2-254">L’implémentation de SetEncodingProperties est présentée dans la section « créer l’objet ASF ContentInfo » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="e8fc2-255">Créer un type de média vidéo compressé</span><span class="sxs-lookup"><span data-stu-id="e8fc2-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="e8fc2-256">Si vous souhaitez inclure un flux vidéo dans le fichier de sortie, créez un type de vidéo encodé de façon complète.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="e8fc2-257">Le type de support complet doit inclure la vitesse de transmission souhaitée et les données privées du codec.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="e8fc2-258">Il existe deux façons de créer un type de média vidéo complet.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="e8fc2-259">Créez un type de média vide et copiez les attributs de type de média à partir du type de vidéo source et remplacez l’attribut de sous- [**\_ \_ type MF MT**](mf-mt-subtype-attribute.md) par la constante GUID MFVideoFormat \_ WMV3.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="e8fc2-260">Un type de vidéo complet doit avoir les attributs suivants définis :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="e8fc2-261">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e8fc2-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="e8fc2-262">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="e8fc2-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="e8fc2-263">\_fréquence d' \_ images MF MF \_</span><span class="sxs-lookup"><span data-stu-id="e8fc2-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="e8fc2-264">\_taille de \_ trame MF MF \_</span><span class="sxs-lookup"><span data-stu-id="e8fc2-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="e8fc2-265">\_ \_ mode entrelacé MF-MT \_</span><span class="sxs-lookup"><span data-stu-id="e8fc2-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="e8fc2-266">\_ \_ \_ rapport hauteur/largeur des pixels \_ MF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="e8fc2-267">\_vitesse de \_ \_ transmission moy. MF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="e8fc2-268">\_ \_ données utilisateur MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="e8fc2-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="e8fc2-269">L’exemple de code suivant crée un type de vidéo compressé à partir du type de vidéo de la source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-269">The following code example creates a compressed video type from the source's video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   <span data-ttu-id="e8fc2-270">Procurez-vous un type de média compatible à partir de l’encodeur vidéo Windows Media en définissant les propriétés d’encodage, puis en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="e8fc2-271">Cette méthode retourne le type partiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-271">This method returns the partial type.</span></span> <span data-ttu-id="e8fc2-272">Veillez à convertir le type partiel en un type complet en ajoutant les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="e8fc2-273">Définissez la vitesse de transmission vidéo dans l’attribut vitesse de [**\_ \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="e8fc2-274">Ajoutez des données privées de codec en définissant l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="e8fc2-275">Pour obtenir des instructions détaillées, consultez « données de codec privées » dans [configuration d’un encodeur WMV](configuring-a-wmv-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="e8fc2-276">Comme [**IWMCodecPrivateData :: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) vérifie la vitesse de transmission avant de retourner les données privées du codec, veillez à définir la vitesse de transmission avant d’obtenir les données privées du codec.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="e8fc2-277">L’exemple de code suivant crée un type de vidéo compressé en obtenant un type compatible à partir de l’encodeur Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="e8fc2-278">Il crée également un type de vidéo non compressé et le définit comme entrée de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="e8fc2-279">Elle est implémentée dans la fonction d’assistance CreateUncompressedVideoType.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="e8fc2-280">GetOutputTypeFromWMVEncoder convertit le type partiel retourné en un type complet en ajoutant des données privées de codec.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="e8fc2-281">L’implémentation de SetEncodingProperties est présentée dans la section « créer l’objet ASF ContentInfo » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    <span data-ttu-id="e8fc2-282">L’exemple de code suivant crée un type de vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-282">The following code example creates an uncompressed video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    <span data-ttu-id="e8fc2-283">L’exemple de code suivant ajoute des données privées de codec au type de média vidéo spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-283">The following code example adds codec private data to the specified video media type.</span></span>

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="e8fc2-284">Créer l’objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="e8fc2-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="e8fc2-285">L’objet ASF ContentInfo est un composant de niveau WMContainer conçu principalement pour stocker les informations relatives aux objets d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="e8fc2-286">Le récepteur de fichiers ASF implémente l’objet ContentInfo afin de stocker les informations (dans une banque de propriétés) qui seront utilisées pour écrire l’objet d’en-tête ASF du fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="e8fc2-287">Pour ce faire, vous devez créer et configurer l’ensemble d’informations suivant sur l’objet ContentInfo avant de démarrer la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="e8fc2-288">Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo vide.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="e8fc2-289">L’exemple de code suivant crée un objet ContentInfo vide.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="e8fc2-290">Appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) pour récupérer la Banque de propriétés au niveau du flux du récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="e8fc2-291">Dans cet appel, vous devez transmettre le numéro de flux que vous avez affecté au flux lors de la création du profil ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="e8fc2-292">Définissez les [propriétés d’encodage](configuring-the-encoder.md) au niveau du flux dans la Banque de propriétés de flux du récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="e8fc2-293">Pour plus d’informations, consultez « Propriétés d’encodage de flux » dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="e8fc2-294">L’exemple de code suivant définit les propriétés de niveau de flux dans la Banque de propriétés du récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    <span data-ttu-id="e8fc2-295">L’exemple de code suivant montre l’implémentation de SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="e8fc2-296">Cette fonction définit les propriétés d’encodage de niveau flux pour CBR et VBR.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="e8fc2-297">Appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) pour récupérer la Banque de propriétés globale du récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="e8fc2-298">Dans cet appel, vous devez passer 0 dans le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="e8fc2-299">Pour plus d’informations, consultez « Propriétés globales du récepteur de fichiers » dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="e8fc2-300">Définissez la valeur de la variable [**MFPKEY ASFMEDIASINK de la \_ vitesse de \_ \_ transmission**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) par variante pour \_ que les valeurs de compartiment avec fuite dans le multiplexeur ASF soient correctement ajustées.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="e8fc2-301">Pour plus d’informations sur cette propriété, consultez « initialisation du multiplexeur et paramètres des compartiments de fuites » dans [création de l’objet multiplexeur](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="e8fc2-302">L’exemple de code suivant définit les propriétés de niveau de flux dans la Banque de propriétés du récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="e8fc2-303">D’autres propriétés peuvent être définies au niveau global pour le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="e8fc2-304">Pour plus d’informations, consultez « Configuration de l’objet ContentInfo avec les paramètres de l’encodeur » dans [définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="e8fc2-305">Vous allez utiliser le fichier ASF ContentInfo configuré pour créer un objet d’activation pour le récepteur de fichiers ASF (décrit dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="e8fc2-306">Si vous créez un récepteur de fichiers out-of-process ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), c’est-à-dire en utilisant un objet d’activation, vous pouvez utiliser l’objet ContentInfo configuré pour instancier le récepteur multimédia ASF (décrit dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="e8fc2-307">Si vous créez un récepteur de fichiers in-process ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), au lieu de créer l’objet ContentInfo vide comme décrit à l’étape 1, vous pouvez obtenir une référence à l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) en appelant **IMFMediaSink :: QueryInterface** sur le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="e8fc2-308">Vous devez ensuite configurer l’objet ContentInfo comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="e8fc2-309">Créer le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-309">Create the ASF File Sink</span></span>

<span data-ttu-id="e8fc2-310">Dans cette étape du didacticiel, vous allez utiliser le fichier ASF ContentInfo, que vous avez créé à l’étape précédente, pour créer un objet d’activation pour le récepteur de fichiers ASF en appelant la fonction [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="e8fc2-311">Pour plus d’informations, consultez [création du récepteur de fichiers ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="e8fc2-312">L’exemple de code suivant crée l’objet d’activation pour le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="e8fc2-313">Créer la topologie d’encodage partiel</span><span class="sxs-lookup"><span data-stu-id="e8fc2-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="e8fc2-314">Ensuite, vous allez créer une topologie d’encodage partielle en créant des nœuds de topologie pour la source du média, les encodeurs Windows Media requis et le récepteur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="e8fc2-315">Après avoir ajouté les nœuds de topologie, vous allez connecter les nœuds source, transformation et récepteur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="e8fc2-316">Avant d’ajouter des nœuds de topologie, vous devez créer un objet de topologie vide en appelant [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="e8fc2-317">Créer le nœud de topologie source pour la source du média</span><span class="sxs-lookup"><span data-stu-id="e8fc2-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="e8fc2-318">Dans cette étape, vous allez créer le nœud de topologie source pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="e8fc2-319">Pour créer ce nœud, vous avez besoin des références suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="e8fc2-320">Pointeur vers la source du média que vous avez créée à l’étape décrite dans la section « créer la source du média » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="e8fc2-321">Pointeur vers le descripteur de présentation pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="e8fc2-322">Vous pouvez obtenir une référence à l’interface IMFPresentationDescriptor de la source du média en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="e8fc2-323">Pointeur vers le descripteur de flux pour chaque flux dans la source du média pour laquelle vous avez créé un flux cible à l’étape décrite dans la section « créer l’objet profil ASF » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="e8fc2-324">Pour plus d’informations sur la création de nœuds sources et d’exemples de code, consultez [création de nœuds sources](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="e8fc2-325">L’exemple de code suivant crée une topologie partielle en ajoutant le nœud source et les nœuds de transformation requis.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="e8fc2-326">Ce code appelle les fonctions d’assistance AddSourceNode et AddTransformOutputNodes.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="e8fc2-327">Ces fonctions sont incluses plus loin dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-327">These functions are included later in this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



<span data-ttu-id="e8fc2-328">L’exemple de code suivant crée et ajoute le nœud de topologie source à la topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="e8fc2-329">Elle prend des pointeurs vers un objet de topologie précédemment, la source du média pour énumérer les flux sources, le descripteur de présentation de la source du média et le descripteur de flux de la source du média.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="e8fc2-330">L’appelant reçoit un pointeur vers le nœud de topologie source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-330">The caller receives a pointer to the source topology node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="e8fc2-331">Instancier les encodeurs requis et créer les nœuds de transformation</span><span class="sxs-lookup"><span data-stu-id="e8fc2-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="e8fc2-332">Le pipeline Media Foundation n’insère pas automatiquement les encodeurs Windows Media requis pour les flux qu’il doit Encoder.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="e8fc2-333">L’application doit ajouter les encodeurs manuellement.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-333">The application must add the encoders manually.</span></span> <span data-ttu-id="e8fc2-334">Pour ce faire, énumérez les flux dans le profil ASF que vous avez créé à l’étape décrite dans la section « créer l’objet profil ASF » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="e8fc2-335">Pour chaque flux dans la source et le flux correspondant dans le profil, instanciez les encodeurs requis.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="e8fc2-336">Pour cette étape, vous avez besoin d’un pointeur vers l’objet d’activation pour le récepteur de fichiers que vous avez créé à l’étape décrite dans la section « créer le récepteur de fichiers ASF » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="e8fc2-337">Pour obtenir une vue d’ensemble de la création d’encodeurs par le biais d’objets d’activation, consultez [utilisation des objets d’activation d’un](using-an-encoder-s-activation-objects.md)encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="e8fc2-338">La procédure suivante décrit les étapes requises pour instancier les encodeurs requis.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="e8fc2-339">Pour obtenir une référence à l’objet ContentInfo du récepteur, appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sur le récepteur de fichiers Activate, puis interrogez [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) à partir du récepteur de fichiers en appelant **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="e8fc2-340">Récupérez le profil ASF associé à l’objet ContentInfo en appelant [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="e8fc2-341">Énumérer les flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="e8fc2-342">Pour cela, vous avez besoin du nombre de flux et d’une référence à l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) de chaque flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="e8fc2-343">Appelez les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="e8fc2-344">**IMFASFProfile::GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="e8fc2-345">**IMFASFProfile :: GetStream**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="e8fc2-346">Pour chaque flux, récupérez le type principal et les propriétés d’encodage du flux à partir de l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="e8fc2-347">Appelez les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="e8fc2-348">**IMFASFStreamConfig::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="e8fc2-349">**IMFMediaType::GetMajorType**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="e8fc2-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="e8fc2-351">Pour cet appel, vous avez besoin du numéro de flux récupéré par l’appel de [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="e8fc2-352">Selon le type de flux, audio ou vidéo, instanciez l’objet d’activation pour l’encodeur en appelant [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="e8fc2-353">Pour appeler ces fonctions, vous avez besoin des références suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="e8fc2-354">Pointeur vers le type de média du flux récupéré par [**IMFASFStreamConfig :: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="e8fc2-355">Pointeur vers le magasin de propriétés d’encodage du flux récupéré par [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="e8fc2-356">En passant un pointeur vers la Banque de propriétés, les propriétés de flux définies dans le récepteur de fichiers sont copiées sur la table MFT de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="e8fc2-357">Mettez à jour le paramètre de compartiment avec fuite pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="e8fc2-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) définit le type de sortie sur la MFT de l’encodeur sous-jacent pour le codec audio Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="e8fc2-359">Une fois que le type de média de sortie est défini, l’encodeur obtient la vitesse de transmission moyenne à partir du type de média de sortie, calcule la vitesse de transmission de la fenêtre de mémoire tampon et définit les valeurs de compartiment avec fuite qui seront utilisées pendant la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="e8fc2-360">Vous pouvez mettre à jour ces valeurs dans le récepteur de fichiers en interrogeant l’encodeur ou en définissant des valeurs personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="e8fc2-361">Pour mettre à jour les valeurs, vous avez besoin de l’ensemble d’informations suivant :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="e8fc2-362">Vitesse de transmission moyenne : obtient la vitesse de transmission moyenne de l’attribut nombre moyen d' [**\_ \_ \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) de l’ensemble des octets audio MF</span><span class="sxs-lookup"><span data-stu-id="e8fc2-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="e8fc2-363">Fenêtre de mémoire tampon : vous pouvez la récupérer en appelant [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="e8fc2-364">Taille de la mémoire tampon initiale : définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="e8fc2-365">Créez un tableau de valeurs DWORD et définissez la valeur dans la [**propriété \_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigée \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) du récepteur de flux audio.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="e8fc2-366">Si vous ne fournissez pas les valeurs mises à jour, la session multimédia les définit de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="e8fc2-367">Pour plus d’informations, consultez [le modèle de mémoire tampon de compartiment](the-leaky-bucket-buffer-model.md)perdu.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="e8fc2-368">Les objets d’activation créés à l’étape 5 doivent être ajoutés à la topologie comme des nœuds de topologie de transformation.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="e8fc2-369">Pour plus d’informations et pour obtenir un exemple de code, consultez « Création d’un nœud de transformation à partir d’un objet d’activation » dans [création de nœuds de transformation](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="e8fc2-370">L’exemple de code suivant crée et ajoute l’activation de l’encodeur requis.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="e8fc2-371">Elle prend des pointeurs vers un objet de topologie précédemment créé, l’objet d’activation du récepteur de fichiers et le type de média du flux source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="e8fc2-372">Il appelle également AddOutputNode (Voir l’exemple de code suivant) qui crée et ajoute le nœud récepteur à la topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="e8fc2-373">L’appelant reçoit un pointeur vers le nœud de topologie source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-373">It The caller receives a pointer to the source topology node.</span></span>


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="e8fc2-374">Créer les nœuds de topologie de sortie pour le récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="e8fc2-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="e8fc2-375">Au cours de cette étape, vous allez créer le nœud de topologie de sortie pour le récepteur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="e8fc2-376">Pour créer ce nœud, vous avez besoin des références suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="e8fc2-377">Pointeur vers l’objet d’activation que vous avez créé à l’étape décrite dans la section « créer le récepteur de fichiers ASF » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="e8fc2-378">Les numéros de flux pour identifier les récepteurs de flux ajoutés au récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="e8fc2-379">Les numéros de flux correspondent à l’identification du flux qui a été définie lors de la création du flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="e8fc2-380">Pour plus d’informations sur la création de nœuds de sortie et d’exemple de code, consultez « Création d’un nœud de sortie à partir d’un objet d’activation » dans [création de nœuds de sortie](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="e8fc2-381">Si vous n’utilisez pas l’objet d’activation pour le récepteur de fichiers, vous devez énumérer les récepteurs de flux dans le récepteur de fichiers ASF et définir chaque récepteur de flux en tant que nœud de sortie dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="e8fc2-382">Pour plus d’informations sur l’énumération du récepteur de flux, consultez « énumération des récepteurs de flux » dans [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="e8fc2-383">L’exemple de code suivant crée et ajoute le nœud récepteur à la topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="e8fc2-384">Elle prend des pointeurs vers un objet de topologie précédemment créé, l’objet d’activation du récepteur de fichiers et le numéro d’identification du flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="e8fc2-385">L’appelant reçoit un pointeur vers le nœud de topologie source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-385">It The caller receives a pointer to the source topology node.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



<span data-ttu-id="e8fc2-386">L’exemple de code suivant énumère les récepteurs de flux pour un récepteur multimédia donné.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="e8fc2-387">Connecter les nœuds source, de transformation et récepteur</span><span class="sxs-lookup"><span data-stu-id="e8fc2-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="e8fc2-388">Au cours de cette étape, vous allez connecter le nœud source au nœud de transformation qui référence l’activation de l’encodage que vous avez créée à l’étape décrite dans la section « instancier les encodeurs requis et créer les nœuds de transformation » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="e8fc2-389">Le nœud de transformation sera connecté au nœud de sortie contenant l’objet d’activation pour le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="e8fc2-390">Gestion de la session d’encodage</span><span class="sxs-lookup"><span data-stu-id="e8fc2-390">Handling the Encoding Session</span></span>

<span data-ttu-id="e8fc2-391">À l’étape, vous allez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="e8fc2-392">Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer une session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="e8fc2-393">Appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie d’encodage sur la session.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="e8fc2-394">Si l’appel se termine, la session de média évalue les nœuds de topologie et insère des objets de transformation supplémentaires tels qu’un décodeur qui convertit la source compressée spécifiée en échantillons non compressés en un flux en tant qu’entrée dans l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="e8fc2-395">Appelez [**IMFMediaSession :: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) pour demander les événements déclenchés par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="e8fc2-396">Dans la boucle d’événements, vous allez démarrer et fermer la session d’encodage en fonction des événements déclenchés par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="e8fc2-397">L’appel de [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) produit une session multimédia déclenchant l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec \_ l' \_ indicateur prêt TOPOSTATUS Ready défini.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="e8fc2-398">Tous les événements sont générés de manière asynchrone et une application peut récupérer ces événements de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="e8fc2-399">Étant donné que l’application de ce didacticiel est une application console et que le blocage des threads d’interface utilisateur n’est pas un problème, nous obtenons les événements de la session de média de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="e8fc2-400">Pour récupérer les événements de façon asynchrone, votre application doit implémenter l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="e8fc2-401">Pour plus d’informations et pour obtenir un exemple d’implémentation de cette interface, consultez « Gestion des événements de session » dans [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="e8fc2-402">Dans la boucle d’événements pour l’obtention d’événements de session multimédia, attendez l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) déclenché lorsque [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se termine et que la topologie est résolue.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="e8fc2-403">Lors de l’obtention de l’événement MESessionTopologyStatus, démarrez la session d’encodage en appelant [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="e8fc2-404">La session multimédia génère l’événement [MEEndOfPresentation](meendofpresentation.md) lorsque toutes les opérations d’encodage sont terminées.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="e8fc2-405">Cet événement doit être géré pour l’encodage VBR et est abordé dans la section suivante « mettre à jour les propriétés d’encodage sur le récepteur de fichiers pour l’encodage VBR » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="e8fc2-406">La session multimédia génère l’objet d’en-tête ASF et finalise le fichier lorsque la session d’encodage est terminée, puis déclenche l’événement [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="e8fc2-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="e8fc2-407">Cet événement doit être géré en effectuant des opérations d’arrêt appropriées sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="e8fc2-408">Pour commencer les opérations d’arrêt, appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="e8fc2-409">Une fois la session d’encodage fermée, vous ne pouvez pas définir une autre topologie pour l’encodage sur la même instance de session de support.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="e8fc2-410">Pour encoder un autre fichier, la session de média en cours doit être fermée et libérée et la nouvelle topologie doit être définie sur une session multimédia nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="e8fc2-411">L’exemple de code suivant crée la session multimédia, définit la topologie d’encodage et gère les événements de session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="e8fc2-412">L’exemple de code suivant crée la session multimédia, définit la topologie d’encodage et contrôle la session d’encodage en gérant les événements de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="e8fc2-413">Mettre à jour les propriétés d’encodage dans le récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="e8fc2-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="e8fc2-414">Certaines propriétés d’encodage, telles que la vitesse de transmission d’encodage et les valeurs de compartiment de fuite exacte, ne sont pas connues tant que l’encodage n’est pas terminé, en particulier pour l’encodage VBR.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="e8fc2-415">Pour obtenir les valeurs correctes, l’application doit attendre l’événement [MEEndOfPresentation](meendofpresentation.md) qui indique que la session d’encodage est terminée.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="e8fc2-416">Les valeurs de compartiment avec fuite doivent être mises à jour dans le récepteur afin que l’objet d’en-tête ASF puisse refléter les valeurs précises.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="e8fc2-417">La procédure suivante décrit les étapes requises pour parcourir les nœuds de la topologie d’encodage afin d’extraire le nœud récepteur de fichiers et de définir les propriétés de compartiment perdues requises.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="e8fc2-418">**Pour mettre à jour les valeurs des propriétés de publication de l’encodage sur le récepteur de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="e8fc2-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="e8fc2-419">Appelez [**IMFTopology :: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) pour récupérer la collection de nœuds de sortie à partir de la topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="e8fc2-420">Pour chaque nœud, vous pouvez obtenir un pointeur vers le récepteur de flux dans le nœud en appelant [**IMFTopologyNode :: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="e8fc2-421">Recherchez l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) sur le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retourné par **IMFTopologyNode :: GetObject**.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="e8fc2-422">Pour chaque récepteur de flux, récupérez le nœud en aval (encodeur) en appelant [**IMFTopologyNode :: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="e8fc2-423">Interrogez le nœud pour obtenir le pointeur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) à partir du nœud de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="e8fc2-424">Interrogez l’encodeur pour le pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour obtenir la Banque de propriétés d’encodage à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="e8fc2-425">Interrogez le récepteur de flux du pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour obtenir la Banque de propriétés du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="e8fc2-426">Appelez [**IPropertyStore :: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour récupérer les valeurs de propriété requises à partir de la Banque de propriétés de l’encodeur et les copier dans la Banque de propriétés du récepteur de flux en appelant **IPropertyStore :: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="e8fc2-427">Le tableau suivant indique les valeurs des propriétés de publication de l’encodage qui doivent être définies sur le récepteur de flux pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="e8fc2-428">Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="e8fc2-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="e8fc2-429">Nom de la propriété (GetValue)</span><span class="sxs-lookup"><span data-stu-id="e8fc2-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="e8fc2-430">Nom de la propriété (SetValue)</span><span class="sxs-lookup"><span data-stu-id="e8fc2-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8fc2-431">Encodage à vitesse binaire constante</span><span class="sxs-lookup"><span data-stu-id="e8fc2-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="e8fc2-432">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="e8fc2-433">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="e8fc2-434">MFPKEY \_ Stat \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="e8fc2-435">MFPKEY \_ Stat \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="e8fc2-436">Encodage de la vitesse de transmission variable basée sur la qualité</span><span class="sxs-lookup"><span data-stu-id="e8fc2-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="e8fc2-437">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="e8fc2-438">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="e8fc2-439">MFPKEY \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="e8fc2-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="e8fc2-440">MFPKEY \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="e8fc2-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="e8fc2-441">MFPKEY \_ Stat \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="e8fc2-442">MFPKEY \_ Stat \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="e8fc2-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="e8fc2-443">MFPKEY \_ Stat \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="e8fc2-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="e8fc2-444">MFPKEY \_ Stat \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="e8fc2-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="e8fc2-445">L’exemple de code suivant définit les valeurs de propriété postérieures à l’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-445">The following code example sets the post-encoding property values.</span></span>


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a><span data-ttu-id="e8fc2-446">Implémenter main</span><span class="sxs-lookup"><span data-stu-id="e8fc2-446">Implement Main</span></span>

<span data-ttu-id="e8fc2-447">L’exemple de code suivant montre la fonction principale de votre application console.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-447">The following code example shows the main function of your console application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a><span data-ttu-id="e8fc2-448">Tester le fichier de sortie</span><span class="sxs-lookup"><span data-stu-id="e8fc2-448">Test the Output File</span></span>

<span data-ttu-id="e8fc2-449">La liste suivante décrit une liste de vérification pour tester le fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="e8fc2-450">Ces valeurs peuvent être vérifiées dans la boîte de dialogue Propriétés du fichier que vous pouvez afficher en cliquant avec le bouton droit sur le fichier encodé et en sélectionnant **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="e8fc2-451">Le chemin d’accès du fichier encodé est exact.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="e8fc2-452">La taille du fichier est supérieure à zéro Ko et la durée de lecture correspond à la durée du fichier source.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="e8fc2-453">Pour le flux vidéo, vérifiez la largeur et la hauteur du frame, ainsi que la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="e8fc2-454">Ces valeurs doivent correspondre aux valeurs que vous avez spécifiées dans le profil ASF que vous avez créé à l’étape décrite dans la section « créer l’objet de profil ASF ».</span><span class="sxs-lookup"><span data-stu-id="e8fc2-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="e8fc2-455">Pour le flux audio, la vitesse de transmission doit être proche de la valeur que vous avez spécifiée sur le type de média cible.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="e8fc2-456">Ouvrez le fichier dans le lecteur Windows Media et vérifiez la qualité de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="e8fc2-457">Ouvrez le fichier ASF dans ASFViewer pour afficher la structure d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="e8fc2-458">Cet outil peut être téléchargé à partir de ce [site Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="e8fc2-459">Codes d’erreur courants et conseils de débogage</span><span class="sxs-lookup"><span data-stu-id="e8fc2-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="e8fc2-460">La liste suivante décrit les codes d’erreur courants que votre peut recevoir et les conseils de débogage.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="e8fc2-461">L’appel à [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) bloque l’application.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="e8fc2-462">Assurez-vous que vous avez initialisé la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="e8fc2-463">Cette fonction configure la plateforme asynchrone qui est utilisée par toutes les méthodes qui démarrent des opérations asynchrones, telles que [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), en interne.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="e8fc2-464">[**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) retourne HRESULT 0X80070002 «le système ne peut pas trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="e8fc2-465">Assurez-vous que le nom du fichier d’entrée spécifié par l’utilisateur dans le premier argument existe.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="e8fc2-466">HRESULT 0x80070020 "le processus ne peut pas accéder au fichier, car il est utilisé par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="e8fc2-467">"</span><span class="sxs-lookup"><span data-stu-id="e8fc2-467">"</span></span>

    <span data-ttu-id="e8fc2-468">Assurez-vous que les fichiers d’entrée et de sortie ne sont pas en cours d’utilisation par une autre ressource du système.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="e8fc2-469">Les appels aux méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retournent MF \_ E \_ INVALIDMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="e8fc2-470">Assurez-vous que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="e8fc2-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="e8fc2-471">Le type d’entrée ou le type de sortie que vous avez spécifié est compatible avec les types de médias pris en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="e8fc2-472">Les types de média que vous avez spécifiés sont terminés.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-472">The media types that you specified are complete.</span></span> <span data-ttu-id="e8fc2-473">Pour que les types de média soient terminés, consultez les attributs requis dans les sections « créer un type de média audio compressé » et « créer un type de média vidéo compressé » de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="e8fc2-474">Assurez-vous que vous avez défini la vitesse de transmission cible sur le type de média partiel auquel vous ajoutez les données privées du codec.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="e8fc2-475">La session multimédia renvoie \_ \_ le type D3D non pris en charge MF E \_ \_ dans l’état de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="e8fc2-476">Cette erreur est retournée lorsque le type de média de la source indique un mode entrelacé mixte qui n’est pas pris en charge par Windows Media Video encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="e8fc2-477">Si votre type de média vidéo compressé est défini pour utiliser le mode progressive, le pipeline doit utiliser une transformation de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="e8fc2-478">Étant donné que le pipeline ne parvient pas à trouver une correspondance (indiquée par ce code d’erreur), vous devez insérer manuellement un décodeur (processeur vidéo de transcodage) entre le décodeur et les nœuds de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="e8fc2-479">La session multimédia renvoie E \_ INVALIDARG dans l’état de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="e8fc2-480">Cette erreur est retournée lorsque les attributs de type de média de la source ne sont pas compatibles avec les attributs du type de média de sortie défini sur l’encodeur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="e8fc2-481">[**IWMCodecPrivateData :: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) retourne HRESULT 0X80040203 « une erreur de syntaxe s’est produite lors de la tentative d’évaluation d’une chaîne de requête »</span><span class="sxs-lookup"><span data-stu-id="e8fc2-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="e8fc2-482">Assurez-vous que le type d’entrée est défini sur la MFT de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8fc2-483">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8fc2-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8fc2-484">Composants ASF de couche de pipeline</span><span class="sxs-lookup"><span data-stu-id="e8fc2-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
