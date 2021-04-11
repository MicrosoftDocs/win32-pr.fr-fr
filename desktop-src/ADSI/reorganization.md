---
title: Réorganisation
description: L’Organisation des ventes a été déplacée vers une nouvelle organisation \ 8212 ; \ 0034 ; Ventes et support. \ 0034 ; Julie Bankert a été promue au vice-président et va mener la nouvelle organisation.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Réorganisation de l’ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028555"
---
# <a name="reorganization"></a><span data-ttu-id="0fee1-105">Réorganisation</span><span class="sxs-lookup"><span data-stu-id="0fee1-105">Reorganization</span></span>

<span data-ttu-id="0fee1-106">L’Organisation des ventes a été déplacée vers une nouvelle organisation (« ventes et support »).</span><span class="sxs-lookup"><span data-stu-id="0fee1-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="0fee1-107">Julie Bankert a été promue au vice-président et va mener la nouvelle organisation.</span><span class="sxs-lookup"><span data-stu-id="0fee1-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="0fee1-108">Joe worden, administrateur de l’entreprise, doit déplacer l’unité d’organisation Sales vers une nouvelle unité d’organisation, sales et support.</span><span class="sxs-lookup"><span data-stu-id="0fee1-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="0fee1-109">Avec cet exemple de code, tous les objets de l’unité d’organisation Sales, y compris les sous-unités d’organisation, sont déplacés vers la nouvelle unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="0fee1-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="0fee1-110">Joe peut à présent déplacer Julie vers l’unité d’organisation Sales and support.</span><span class="sxs-lookup"><span data-stu-id="0fee1-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="0fee1-111">N’oubliez pas que le lien Manager-direct Report entre Julie Bankert et Chris Gray est automatiquement mis à jour par Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0fee1-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="0fee1-112">**Pour créer un rapport de Active Directory**</span><span class="sxs-lookup"><span data-stu-id="0fee1-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="0fee1-113">Ouvrez Visual Basic version 6,0 et, lorsque vous êtes invité à entrer le type de projet, sélectionnez **projet de données**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="0fee1-114">Sur le **projet de données**, double-cliquez sur **données Environment1**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="0fee1-115">Dans la fenêtre **environnement de données** , cliquez avec le bouton droit sur l’objet de connexion **(Connection1)** et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="0fee1-116">Sélectionnez **OLE DB fournisseur pour les services d’annuaire Microsoft**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="0fee1-117">Sélectionnez **utiliser la sécurité intégrée de Windows NT**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="0fee1-118">Cela crée un objet de connexion.</span><span class="sxs-lookup"><span data-stu-id="0fee1-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="0fee1-119">Cliquez à nouveau avec le bouton droit sur la fenêtre **environnement de données** pour sélectionner **Ajouter une commande**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="0fee1-120">Cliquez avec le bouton droit sur l’objet **Command1** et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="0fee1-121">La boîte de dialogue **Propriétés de commande1** suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0fee1-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![boîte de dialogue Propriétés de commande1](images/adadsi3.png)

7.  <span data-ttu-id="0fee1-123">Cliquez sur la case d’option **instruction SQL** et tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0fee1-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="0fee1-124">Sélectionnez nom, telephoneNumber à partir de « LDAP://DC = fabrikam, DC = com », où objectCategory = « Person » et objectClass = « user »</span><span class="sxs-lookup"><span data-stu-id="0fee1-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="0fee1-125">L’objet **Command** est créé.</span><span class="sxs-lookup"><span data-stu-id="0fee1-125">The **Command** object is created.</span></span> <span data-ttu-id="0fee1-126">Ajoutez l’objet de **commande** au rapport.</span><span class="sxs-lookup"><span data-stu-id="0fee1-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="0fee1-127">Double-cliquez sur **données Report1** dans la fenêtre **projet** .</span><span class="sxs-lookup"><span data-stu-id="0fee1-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="0fee1-128">Faites glisser l’objet **Command1** de la fenêtre **DataEnvironment1** vers la section **Détails** de la fenêtre **rapport de données** .</span><span class="sxs-lookup"><span data-stu-id="0fee1-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="0fee1-129">Dans **Propriétés de DataReport1**, pour **DataSource**, sélectionnez **DataEnvironment1** dans le menu déroulant, puis sélectionnez **Command1** dans le champ **DataMember** .</span><span class="sxs-lookup"><span data-stu-id="0fee1-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="0fee1-130">Dans la fenêtre projet, cliquez avec le bouton droit sur **projet de données**, puis sélectionnez **Propriétés de DataProject**.</span><span class="sxs-lookup"><span data-stu-id="0fee1-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="0fee1-131">Dans la fenêtre de boîte de dialogue **DataProject-propriétés du projet** , sous **objet de démarrage**, sélectionnez **DataReport1** dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="0fee1-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="0fee1-132">Cliquez sur **OK** pour enregistrer.</span><span class="sxs-lookup"><span data-stu-id="0fee1-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="0fee1-133">Compilation.</span><span class="sxs-lookup"><span data-stu-id="0fee1-133">Compile.</span></span> <span data-ttu-id="0fee1-134">La boîte de dialogue **DataReport1** suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0fee1-134">The following **DataReport1** dialog box will appear.</span></span>

    ![boîte de dialogue datareport1](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="0fee1-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fee1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fee1-137">Jointure de données hétérogènes</span><span class="sxs-lookup"><span data-stu-id="0fee1-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




