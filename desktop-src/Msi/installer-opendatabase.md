---
description: La méthode OpenDatabase de l’objet installer ouvre une base de données existante ou en crée une nouvelle, en retournant un objet Database. Elle génère une erreur si l’objet de base de données ne peut pas être créé et ouvert avec succès.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532916"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="ea896-104">Installer. OpenDatabase, méthode</span><span class="sxs-lookup"><span data-stu-id="ea896-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="ea896-105">La méthode **OpenDatabase** de l’objet [**installer**](installer-object.md) ouvre une base de données existante ou en crée une nouvelle, en retournant un objet [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ea896-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="ea896-106">Elle génère une erreur si l’objet **de base de données** ne peut pas être créé et ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="ea896-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea896-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea896-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="ea896-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea896-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea896-109">*name*</span><span class="sxs-lookup"><span data-stu-id="ea896-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="ea896-110">Chaîne obligatoire qui contient le nom du chemin d’accès de la base de données.</span><span class="sxs-lookup"><span data-stu-id="ea896-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="ea896-111">Si une chaîne vide est fournie, une base de données temporaire est créée, qui n’est pas persistante.</span><span class="sxs-lookup"><span data-stu-id="ea896-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="ea896-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="ea896-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="ea896-113">Un paramètre de la liste suivante ou une chaîne qui contient le nom du chemin d’accès du nouveau fichier de base de données de sortie sur lequel l’écriture doit être effectuée lors de la validation.</span><span class="sxs-lookup"><span data-stu-id="ea896-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="ea896-114">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ea896-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="ea896-115">Signification</span><span class="sxs-lookup"><span data-stu-id="ea896-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="ea896-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="ea896-117">Ouvre une base de données en lecture seule, pas de modifications persistantes.</span><span class="sxs-lookup"><span data-stu-id="ea896-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="ea896-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="ea896-119">Ouvre une base de données en lecture/écriture en mode de transaction.</span><span class="sxs-lookup"><span data-stu-id="ea896-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="ea896-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="ea896-121">Ouvre une base de données en lecture/écriture directe sans transaction.</span><span class="sxs-lookup"><span data-stu-id="ea896-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="ea896-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="ea896-123">Crée une base de données, en lecture/écriture en mode Transact.</span><span class="sxs-lookup"><span data-stu-id="ea896-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="ea896-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="ea896-125">Crée une base de données, en lecture/écriture en mode direct.</span><span class="sxs-lookup"><span data-stu-id="ea896-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="ea896-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="ea896-127">Ouvre une base de données pour afficher les fichiers de script de publication, tels que les fichiers générés par la méthode [**CreateAdvertiseScript**](installer-createadvertisescript.md) .</span><span class="sxs-lookup"><span data-stu-id="ea896-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="ea896-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="ea896-129">Ajoute cet indicateur pour indiquer un fichier correctif.</span><span class="sxs-lookup"><span data-stu-id="ea896-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea896-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea896-130">Return value</span></span>

<span data-ttu-id="ea896-131">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ea896-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea896-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ea896-132">Remarks</span></span>

<span data-ttu-id="ea896-133">Lorsqu’une base de données est ouverte comme sortie d’une autre base de données, le flux d’informations de synthèse de la base de données de sortie est en fait un miroir en lecture seule de la base de données d’origine et ne peut donc pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="ea896-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="ea896-134">En outre, elle n’est pas conservée avec la base de données.</span><span class="sxs-lookup"><span data-stu-id="ea896-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="ea896-135">Pour créer ou modifier les informations de résumé de la base de données de sortie, vous devez la fermer, puis la rouvrir.</span><span class="sxs-lookup"><span data-stu-id="ea896-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="ea896-136">Pour créer et enregistrer les modifications apportées à une base de données, commencez par ouvrir la base de données en mode transaction (msiOpenDatabaseModeTransact), Create (msiOpenDatabaseModeCreate ou msiOpenDatabaseModeCreateDirect) ou direct (msiOpenDatabaseModeDirect).</span><span class="sxs-lookup"><span data-stu-id="ea896-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="ea896-137">Après avoir apporté les modifications, appelez toujours la méthode [**Commit**](database-commit.md) avant de fermer le handle de base de données.</span><span class="sxs-lookup"><span data-stu-id="ea896-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="ea896-138">La méthode **Commit** vide toutes les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="ea896-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="ea896-139">Appelez toujours la méthode [**Commit**](database-commit.md) sur une base de données qui a été ouverte en mode direct (MsiOpenDatabaseModeDirect ou msiOpenDatabaseModeCreateDirect) avant de fermer la base de données.</span><span class="sxs-lookup"><span data-stu-id="ea896-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="ea896-140">L’échec de cette opération peut endommager la base de données.</span><span class="sxs-lookup"><span data-stu-id="ea896-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="ea896-141">Étant donné que la méthode **OpenDatabase** initie l’accès à la base de données, elle ne peut pas être utilisée avec une installation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ea896-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="ea896-142">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ea896-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea896-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea896-143">Requirements</span></span>



| <span data-ttu-id="ea896-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea896-144">Requirement</span></span> | <span data-ttu-id="ea896-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea896-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea896-146">Version</span><span class="sxs-lookup"><span data-stu-id="ea896-146">Version</span></span><br/> | <span data-ttu-id="ea896-147">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea896-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea896-148">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea896-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea896-149">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea896-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ea896-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ea896-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea896-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea896-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ea896-152">IID</span><span class="sxs-lookup"><span data-stu-id="ea896-152">IID</span></span><br/>     | <span data-ttu-id="ea896-153">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ea896-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




