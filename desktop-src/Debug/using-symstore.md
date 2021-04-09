---
description: SymStore (symstore.exe) est un outil permettant de créer des magasins de symboles. Il est inclus dans le package outils de débogage pour Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Utilisation de SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110710"
---
# <a name="using-symstore"></a><span data-ttu-id="c9f65-104">Utilisation de SymStore</span><span class="sxs-lookup"><span data-stu-id="c9f65-104">Using SymStore</span></span>

<span data-ttu-id="c9f65-105">SymStore (symstore.exe) est un outil permettant de créer des magasins de symboles.</span><span class="sxs-lookup"><span data-stu-id="c9f65-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="c9f65-106">Il est inclus dans le package [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="c9f65-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="c9f65-107">SymStore stocke les symboles dans un format qui permet au débogueur de rechercher les symboles en fonction de l’horodatage et de la taille de l’image (pour un fichier. dbg ou exécutable), ou de la signature et de l’âge (pour un fichier. pdb).</span><span class="sxs-lookup"><span data-stu-id="c9f65-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="c9f65-108">L’avantage du magasin de symboles par rapport au format de stockage de symboles traditionnel est que tous les symboles peuvent être stockés ou référencés sur le même serveur et récupérés par le débogueur sans connaissance préalable du produit contenant le symbole correspondant.</span><span class="sxs-lookup"><span data-stu-id="c9f65-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="c9f65-109">Notez que plusieurs versions des fichiers de symboles. pdb (par exemple, les versions publique et privée) ne peuvent pas être stockées sur le même serveur, car elles contiennent chacune les mêmes signature et âge.</span><span class="sxs-lookup"><span data-stu-id="c9f65-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="c9f65-110">Transactions SymStore</span><span class="sxs-lookup"><span data-stu-id="c9f65-110">SymStore Transactions</span></span>

<span data-ttu-id="c9f65-111">Chaque appel à SymStore est enregistré en tant que transaction.</span><span class="sxs-lookup"><span data-stu-id="c9f65-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="c9f65-112">Il existe deux types de transactions : ajouter et supprimer.</span><span class="sxs-lookup"><span data-stu-id="c9f65-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="c9f65-113">Lorsque le magasin de symboles est créé, un répertoire nommé « 000admin » est créé sous la racine du serveur.</span><span class="sxs-lookup"><span data-stu-id="c9f65-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="c9f65-114">Le répertoire 000admin contient un fichier pour chaque transaction, ainsi que les fichiers journaux Server.txt et History.txt.</span><span class="sxs-lookup"><span data-stu-id="c9f65-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="c9f65-115">Le fichier Server.txt contient une liste de toutes les transactions qui se trouvent actuellement sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c9f65-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="c9f65-116">Le fichier History.txt contient un historique chronologique de toutes les transactions.</span><span class="sxs-lookup"><span data-stu-id="c9f65-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="c9f65-117">Chaque fois que SymStore stocke ou supprime des fichiers de symboles, un nouveau numéro de transaction est créé.</span><span class="sxs-lookup"><span data-stu-id="c9f65-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="c9f65-118">Ensuite, un fichier, dont le nom est ce numéro de transaction, est créé dans 000admin.</span><span class="sxs-lookup"><span data-stu-id="c9f65-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="c9f65-119">Ce fichier contient une liste de tous les fichiers ou pointeurs qui ont été ajoutés au magasin de symboles au cours de cette transaction.</span><span class="sxs-lookup"><span data-stu-id="c9f65-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="c9f65-120">Si une transaction est supprimée, SymStore lit son fichier de transactions pour déterminer les fichiers et les pointeurs à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c9f65-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="c9f65-121">Les options **Add** et **del** spécifient si une transaction d’ajout ou de suppression doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="c9f65-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="c9f65-122">L’inclusion de l’option **/p** avec une opération Add spécifie qu’un pointeur doit être ajouté ; l’omission de l’option **/p** spécifie que le fichier de symboles réel doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="c9f65-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="c9f65-123">Il est également possible de créer le magasin de symboles en deux étapes distinctes.</span><span class="sxs-lookup"><span data-stu-id="c9f65-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="c9f65-124">Dans la première étape, vous utilisez SymStore avec l’option **/x** pour créer un fichier d’index.</span><span class="sxs-lookup"><span data-stu-id="c9f65-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="c9f65-125">Dans la deuxième étape, vous utilisez SymStore avec l’option **/y** pour créer le magasin de fichiers ou de pointeurs à partir des informations contenues dans le fichier d’index.</span><span class="sxs-lookup"><span data-stu-id="c9f65-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="c9f65-126">Il peut s’agir d’une technique utile pour diverses raisons.</span><span class="sxs-lookup"><span data-stu-id="c9f65-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="c9f65-127">Par exemple, cela permet de recréer facilement le magasin de symboles si le magasin est perdu, tant que le fichier d’index existe toujours.</span><span class="sxs-lookup"><span data-stu-id="c9f65-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="c9f65-128">Ou peut-être que l’ordinateur contenant les fichiers de symboles dispose d’une connexion réseau lente à l’ordinateur sur lequel le magasin de symboles sera créé.</span><span class="sxs-lookup"><span data-stu-id="c9f65-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="c9f65-129">Dans ce cas, vous pouvez créer le fichier d’index sur le même ordinateur que les fichiers de symboles, transférer le fichier d’index sur le deuxième ordinateur, puis créer le magasin sur le deuxième ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9f65-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="c9f65-130">Pour obtenir la liste complète de tous les paramètres SymStore, consultez [options de SymStore Command-Line](symstore-command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="c9f65-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="c9f65-131">SymStore ne prend pas en charge les transactions simultanées de plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c9f65-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="c9f65-132">Il est recommandé qu’un utilisateur soit désigné « administrateur » du magasin de symboles et qu’il soit responsable de toutes les transactions **Add** et **del** .</span><span class="sxs-lookup"><span data-stu-id="c9f65-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="c9f65-133">Exemples de transactions</span><span class="sxs-lookup"><span data-stu-id="c9f65-133">Transaction Examples</span></span>

<span data-ttu-id="c9f65-134">Voici deux exemples de SymStore ajout de pointeurs de symboles pour la build 3790 de Windows Server 2003 à \\ \\ SampleDir \\ symsrv :</span><span class="sxs-lookup"><span data-stu-id="c9f65-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="c9f65-135">Dans l’exemple suivant, SymStore ajoute les fichiers de symboles réels pour un projet d’application dans les \\ \\ \\ emplacements AppServer largeapp \\ à \\ \\ TestDir \\ symsrv :</span><span class="sxs-lookup"><span data-stu-id="c9f65-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="c9f65-136">Voici un exemple d’utilisation d’un fichier d’index.</span><span class="sxs-lookup"><span data-stu-id="c9f65-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="c9f65-137">Tout d’abord, SymStore crée un fichier d’index basé sur la collection de fichiers de symboles dans les \\ \\ \\ emplacements AppServer largeapp \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="c9f65-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="c9f65-138">Dans ce cas, le fichier d’index est placé sur un troisième ordinateur, \\ \\ hubserver \\ hubshare.</span><span class="sxs-lookup"><span data-stu-id="c9f65-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="c9f65-139">Vous utilisez l’option **/g** pour spécifier que le préfixe de fichier « \\ \\ largeapp \\ AppServer » peut changer à l’avenir :</span><span class="sxs-lookup"><span data-stu-id="c9f65-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="c9f65-140">Supposons à présent que vous déplaciez tous les fichiers de symboles de la machine \\ \\ largeapp AppServer et que vous les \\ Placez sur \\ \\ myarchive \\ AppServer.</span><span class="sxs-lookup"><span data-stu-id="c9f65-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="c9f65-141">Vous pouvez ensuite créer le magasin de symboles lui-même à partir du fichier d’index \\ \\ hubserver \\ hubshare \\myindex.txt comme suit :</span><span class="sxs-lookup"><span data-stu-id="c9f65-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="c9f65-142">Enfin, voici un exemple de SymStore de suppression d’un fichier ajouté par une transaction précédente.</span><span class="sxs-lookup"><span data-stu-id="c9f65-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="c9f65-143">Consultez la section suivante pour obtenir une explication sur la façon de déterminer l’ID de transaction (dans ce cas, 0000000096).</span><span class="sxs-lookup"><span data-stu-id="c9f65-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="c9f65-144">Fichiers compressés</span><span class="sxs-lookup"><span data-stu-id="c9f65-144">Compressed Files</span></span>

<span data-ttu-id="c9f65-145">SymStore peut être utilisé avec des fichiers compressés de deux manières différentes.</span><span class="sxs-lookup"><span data-stu-id="c9f65-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="c9f65-146">Utilisez SymStore avec l’option **/p** pour stocker des pointeurs vers les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="c9f65-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="c9f65-147">Une fois SymStore terminé, compressez les fichiers auxquels les pointeurs font référence.</span><span class="sxs-lookup"><span data-stu-id="c9f65-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="c9f65-148">Utilisez SymStore avec l’option **/x** pour créer un fichier d’index.</span><span class="sxs-lookup"><span data-stu-id="c9f65-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="c9f65-149">Une fois SymStore terminé, compressez les fichiers listés dans le fichier d’index.</span><span class="sxs-lookup"><span data-stu-id="c9f65-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="c9f65-150">Utilisez ensuite SymStore avec l’option **/y** (et, si vous le souhaitez, l’option **/p** ) pour stocker les fichiers ou les pointeurs vers les fichiers dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="c9f65-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="c9f65-151">(SymStore n’a pas besoin de décompresser les fichiers pour effectuer cette opération.)</span><span class="sxs-lookup"><span data-stu-id="c9f65-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="c9f65-152">Votre serveur de symboles est chargé de décompresser les fichiers lorsqu’ils sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c9f65-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="c9f65-153">Si vous utilisez SymSrv en tant que serveur de symboles, toute compression doit être effectuée à l’aide de l’outil compress.exe qui est distribué avec le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c9f65-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c9f65-154">Les fichiers compressés doivent avoir un trait de soulignement comme dernier caractère dans leurs extensions de fichier (par exemple, Module1. PD \_ ou Module2. db \_ ).</span><span class="sxs-lookup"><span data-stu-id="c9f65-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="c9f65-155">Pour plus d’informations, consultez [utilisation de symsrv](using-symsrv.md).</span><span class="sxs-lookup"><span data-stu-id="c9f65-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="c9f65-156">Fichiers server.txt et history.txt</span><span class="sxs-lookup"><span data-stu-id="c9f65-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="c9f65-157">Lorsqu’une transaction est ajoutée, plusieurs éléments d’information sont ajoutés à server.txt et history.txt pour la future capacité de recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f65-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="c9f65-158">Voici un exemple de ligne dans server.txt et history.txt pour une transaction Add :</span><span class="sxs-lookup"><span data-stu-id="c9f65-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="c9f65-159">Il s’agit d’une ligne séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="c9f65-159">This is a comma-separated line.</span></span> <span data-ttu-id="c9f65-160">Les champs sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="c9f65-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="c9f65-161">Champ</span><span class="sxs-lookup"><span data-stu-id="c9f65-161">Field</span></span>      | <span data-ttu-id="c9f65-162">Description</span><span class="sxs-lookup"><span data-stu-id="c9f65-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f65-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="c9f65-163">0000000096</span></span> | <span data-ttu-id="c9f65-164">Numéro d’identification de la transaction, tel qu’il a été créé par SymStore.</span><span class="sxs-lookup"><span data-stu-id="c9f65-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="c9f65-165">add</span><span class="sxs-lookup"><span data-stu-id="c9f65-165">add</span></span>        | <span data-ttu-id="c9f65-166">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="c9f65-166">Type of transaction.</span></span> <span data-ttu-id="c9f65-167">Ce champ peut avoir la valeur **Add** ou **del**.</span><span class="sxs-lookup"><span data-stu-id="c9f65-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="c9f65-168">ptr</span><span class="sxs-lookup"><span data-stu-id="c9f65-168">ptr</span></span>        | <span data-ttu-id="c9f65-169">Indique si des fichiers ou des pointeurs ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="c9f65-169">Whether files or pointers were added.</span></span> <span data-ttu-id="c9f65-170">Ce champ peut être un **fichier** ou un **ptr**.</span><span class="sxs-lookup"><span data-stu-id="c9f65-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="c9f65-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="c9f65-171">10/09/99</span></span>   | <span data-ttu-id="c9f65-172">Date à laquelle la transaction s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c9f65-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="c9f65-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="c9f65-173">00:08:32</span></span>   | <span data-ttu-id="c9f65-174">Heure de début de la transaction.</span><span class="sxs-lookup"><span data-stu-id="c9f65-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="c9f65-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9f65-175">Windows XP</span></span> | <span data-ttu-id="c9f65-176">Produit.</span><span class="sxs-lookup"><span data-stu-id="c9f65-176">Product.</span></span>                                                                            |
| <span data-ttu-id="c9f65-177">fre x86</span><span class="sxs-lookup"><span data-stu-id="c9f65-177">x86 fre</span></span>    | <span data-ttu-id="c9f65-178">Version (facultatif).</span><span class="sxs-lookup"><span data-stu-id="c9f65-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="c9f65-179">Ajouté à partir de</span><span class="sxs-lookup"><span data-stu-id="c9f65-179">Added from</span></span> | <span data-ttu-id="c9f65-180">Commentaire (facultatif)</span><span class="sxs-lookup"><span data-stu-id="c9f65-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="c9f65-181">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="c9f65-181">Unused</span></span>     | <span data-ttu-id="c9f65-182">(Réservé pour une utilisation ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="c9f65-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="c9f65-183">Voici quelques exemples de lignes du fichier de transaction 0000000096.</span><span class="sxs-lookup"><span data-stu-id="c9f65-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="c9f65-184">Chaque ligne enregistre le répertoire et l’emplacement du fichier ou du pointeur qui a été ajouté au répertoire.</span><span class="sxs-lookup"><span data-stu-id="c9f65-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="c9f65-185">Si vous utilisez une transaction **del** pour annuler l' **Ajout** de transactions d’origine, ces lignes sont supprimées de server.txt, et la ligne suivante est ajoutée à history.txt :</span><span class="sxs-lookup"><span data-stu-id="c9f65-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="c9f65-186">Les champs de la transaction de suppression sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="c9f65-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="c9f65-187">Champ</span><span class="sxs-lookup"><span data-stu-id="c9f65-187">Field</span></span>      | <span data-ttu-id="c9f65-188">Description</span><span class="sxs-lookup"><span data-stu-id="c9f65-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="c9f65-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="c9f65-189">0000000105</span></span> | <span data-ttu-id="c9f65-190">Numéro d’identification de la transaction, tel qu’il a été créé par SymStore.</span><span class="sxs-lookup"><span data-stu-id="c9f65-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="c9f65-191">del</span><span class="sxs-lookup"><span data-stu-id="c9f65-191">del</span></span>        | <span data-ttu-id="c9f65-192">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="c9f65-192">Type of transaction.</span></span> <span data-ttu-id="c9f65-193">Ce champ peut avoir la valeur **Add** ou **del**.</span><span class="sxs-lookup"><span data-stu-id="c9f65-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="c9f65-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="c9f65-194">0000000096</span></span> | <span data-ttu-id="c9f65-195">Transaction qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="c9f65-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="c9f65-196">Format de stockage des symboles</span><span class="sxs-lookup"><span data-stu-id="c9f65-196">Symbol Storage Format</span></span>

<span data-ttu-id="c9f65-197">SymStore utilise le système de fichiers lui-même en tant que base de données.</span><span class="sxs-lookup"><span data-stu-id="c9f65-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="c9f65-198">Il crée une grande arborescence de répertoires, avec des noms de répertoires basés sur des horodatages de fichier de symboles, des signatures, de l’âge et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="c9f65-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="c9f65-199">Par exemple, après l’ajout de plusieurs fichiers ACPI. dbg différents au serveur, les répertoires peuvent se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="c9f65-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

<span data-ttu-id="c9f65-200">Dans cet exemple, le chemin de recherche du fichier de symboles ACPI. dbg peut se présenter comme suit : \\ \\ mybuilds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.</span><span class="sxs-lookup"><span data-stu-id="c9f65-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="c9f65-201">Trois fichiers peuvent se trouver dans le répertoire de recherche :</span><span class="sxs-lookup"><span data-stu-id="c9f65-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="c9f65-202">Si le fichier a été stocké, ACPI. dbg y figure.</span><span class="sxs-lookup"><span data-stu-id="c9f65-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="c9f65-203">Si un pointeur était stocké, un fichier appelé file. PTR existe et contient le chemin d’accès au fichier de symboles réel.</span><span class="sxs-lookup"><span data-stu-id="c9f65-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="c9f65-204">Un fichier appelé refs. PTR, qui contient une liste de tous les emplacements actuels pour ACPI. dbg avec cet horodatage et la taille de l’image qui sont actuellement ajoutés au magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="c9f65-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="c9f65-205">L’affichage de la liste de répertoires de \\ \\ mybuilds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040 donne ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c9f65-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="c9f65-206">Le fichier file. PTR contient la chaîne de texte « \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg ».</span><span class="sxs-lookup"><span data-stu-id="c9f65-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="c9f65-207">Étant donné qu’il n’y a aucun fichier nommé ACPI. dbg dans ce répertoire, le débogueur essaiera de trouver le fichier dans \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg.</span><span class="sxs-lookup"><span data-stu-id="c9f65-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="c9f65-208">Le contenu de refs. PTR est utilisé uniquement par SymStore, et non par le débogueur.</span><span class="sxs-lookup"><span data-stu-id="c9f65-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="c9f65-209">Ce fichier contient un enregistrement de toutes les transactions qui ont eu lieu dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="c9f65-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="c9f65-210">Un exemple de ligne de refs. PTR peut être :</span><span class="sxs-lookup"><span data-stu-id="c9f65-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="c9f65-211">Cela montre qu’un pointeur vers \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg a été ajouté avec la transaction « 0000000026 ».</span><span class="sxs-lookup"><span data-stu-id="c9f65-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="c9f65-212">Certains fichiers de symboles restent constants par le biais de différents produits ou builds, ou d’un produit particulier.</span><span class="sxs-lookup"><span data-stu-id="c9f65-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="c9f65-213">Le fichier Msvcrt. pdb en est un exemple.</span><span class="sxs-lookup"><span data-stu-id="c9f65-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="c9f65-214">La réalisation d’un répertoire de \\ \\ mybuilds \\ symsrv \\ Msvcrt. pdb montre que seules deux versions de Msvcrt. pdb ont été ajoutées au serveur de symboles :</span><span class="sxs-lookup"><span data-stu-id="c9f65-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="c9f65-215">Toutefois, le fait de faire d’un répertoire de \\ \\ mybuilds \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 montre que refs. PTR a plusieurs pointeurs dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c9f65-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="c9f65-216">Le contenu de \\ \\ mybuilds \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 \\ refs. PTR est le suivant :</span><span class="sxs-lookup"><span data-stu-id="c9f65-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

<span data-ttu-id="c9f65-217">Cela indique que le même fichier Msvcrt. pdb a été utilisé pour plusieurs générations de symboles stockées sur \\ \\ mybuilds \\ symsrv.</span><span class="sxs-lookup"><span data-stu-id="c9f65-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="c9f65-218">Voici un exemple de répertoire contenant un mélange d’ajouts de fichiers et de pointeurs :</span><span class="sxs-lookup"><span data-stu-id="c9f65-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="c9f65-219">Dans ce cas, refs. PTR a le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="c9f65-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="c9f65-220">Ainsi, les transactions 43, 44 et 45 ont ajouté le même fichier au serveur, et les transactions 46 et 47 ont ajouté des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="c9f65-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="c9f65-221">Si les transactions 43, 44 et 45 sont supprimées, le fichier dbghelp. dbg sera supprimé du répertoire.</span><span class="sxs-lookup"><span data-stu-id="c9f65-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="c9f65-222">Le répertoire présente ensuite le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="c9f65-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="c9f65-223">Désormais, file. PTR contient « \\ \\ sampledir2 \\ bin \\ Symbols \\ Retail \\ dll \\ dbghelp. dbg » et refs. PTR contient</span><span class="sxs-lookup"><span data-stu-id="c9f65-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="c9f65-224">Chaque fois que l’entrée finale dans refs. PTR est un pointeur, le fichier. PTR existe et contient le chemin d’accès au fichier associé.</span><span class="sxs-lookup"><span data-stu-id="c9f65-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="c9f65-225">Chaque fois que l’entrée finale dans refs. PTR est un fichier, aucun fichier. PTR n’existe dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="c9f65-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="c9f65-226">Par conséquent, toute opération de suppression qui supprime l’entrée finale dans refs. PTR peut entraîner la création, la suppression ou la modification de fichier. ptr.</span><span class="sxs-lookup"><span data-stu-id="c9f65-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



