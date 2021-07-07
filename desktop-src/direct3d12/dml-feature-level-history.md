---
title: Historique des niveaux de fonctionnalité DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282548"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="edfd3-103">Historique des niveaux de fonctionnalité DirectML</span><span class="sxs-lookup"><span data-stu-id="edfd3-103">DirectML feature level history</span></span>

<span data-ttu-id="edfd3-104">Pour un historique général des versions de DirectML, consultez [l’historique des versions DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="edfd3-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="edfd3-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="edfd3-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="edfd3-106">Introduit dans DirectML version 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="edfd3-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="edfd3-107">Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="edfd3-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="edfd3-108">Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.</span><span class="sxs-lookup"><span data-stu-id="edfd3-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="edfd3-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="edfd3-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="edfd3-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="edfd3-112">Prise en charge des types de données étendus et du nombre de dimensions pour les opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="edfd3-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="edfd3-113">Pour plus d’informations sur la prise en charge spécifique ajoutée dans [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), consultez la rubrique relative à la structure de chaque opérateur.</span><span class="sxs-lookup"><span data-stu-id="edfd3-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="edfd3-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="edfd3-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="edfd3-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="edfd3-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="edfd3-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="edfd3-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="edfd3-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="edfd3-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="edfd3-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="edfd3-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="edfd3-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="edfd3-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="edfd3-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="edfd3-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="edfd3-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="edfd3-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="edfd3-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="edfd3-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="edfd3-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="edfd3-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="edfd3-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="edfd3-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="edfd3-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="edfd3-132">Introduit dans DirectML version 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="edfd3-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="edfd3-133">Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="edfd3-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="edfd3-134">Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.</span><span class="sxs-lookup"><span data-stu-id="edfd3-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="edfd3-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="edfd3-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="edfd3-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="edfd3-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="edfd3-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="edfd3-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="edfd3-141">Le nombre maximal de dimensions prises en charge pour les opérateurs suivants est passé de 4 à 8.</span><span class="sxs-lookup"><span data-stu-id="edfd3-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="edfd3-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="edfd3-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="edfd3-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="edfd3-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="edfd3-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="edfd3-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="edfd3-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="edfd3-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="edfd3-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="edfd3-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="edfd3-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="edfd3-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="edfd3-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="edfd3-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="edfd3-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="edfd3-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="edfd3-154">Introduit dans DirectML version 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="edfd3-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="edfd3-155">Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="edfd3-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="edfd3-156">Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.</span><span class="sxs-lookup"><span data-stu-id="edfd3-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="edfd3-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="edfd3-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="edfd3-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="edfd3-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="edfd3-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="edfd3-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="edfd3-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="edfd3-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="edfd3-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="edfd3-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="edfd3-164">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="edfd3-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="edfd3-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="edfd3-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="edfd3-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="edfd3-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="edfd3-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="edfd3-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="edfd3-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="edfd3-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="edfd3-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="edfd3-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="edfd3-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="edfd3-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="edfd3-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="edfd3-177">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="edfd3-177">Added the following enhancements.</span></span>

* <span data-ttu-id="edfd3-178">Le nombre maximal de dimensions de tenseur a été augmenté de 5 à 8.</span><span class="sxs-lookup"><span data-stu-id="edfd3-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="edfd3-179">Consultez [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="edfd3-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="edfd3-180">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="edfd3-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="edfd3-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="edfd3-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="edfd3-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="edfd3-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="edfd3-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** et **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="edfd3-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="edfd3-184">**DML_OPERATOR_REDUCE**, lors de l’utilisation de **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="edfd3-185">Les types de données 64 bits suivants ont été ajoutés et sont pris en charge par les opérateurs Select.</span><span class="sxs-lookup"><span data-stu-id="edfd3-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="edfd3-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="edfd3-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="edfd3-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="edfd3-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="edfd3-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="edfd3-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="edfd3-189">Fonctionnalités dépréciées.</span><span class="sxs-lookup"><span data-stu-id="edfd3-189">Deprecated functionality.</span></span>

* <span data-ttu-id="edfd3-190">**DML_REDUCE_FUNCTION_ARGMAX** et **DML_REDUCE_FUNCTION_ARGMIN** ont été dépréciés.</span><span class="sxs-lookup"><span data-stu-id="edfd3-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="edfd3-191">Il est préférable d’utiliser les opérateurs **DML_OPERATOR_ARGMIN** et **DML_OPERATOR_ARGMAX** autonomes à leur place.</span><span class="sxs-lookup"><span data-stu-id="edfd3-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="edfd3-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="edfd3-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="edfd3-193">Introduit dans DirectML version 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="edfd3-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="edfd3-194">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="edfd3-194">Added the following APIs.</span></span>

* [<span data-ttu-id="edfd3-195">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="edfd3-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="edfd3-196">Prise en charge des graphiques d’opérateur (consultez [IDMLDevice1 :: CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="edfd3-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="edfd3-197">Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="edfd3-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="edfd3-198">Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.</span><span class="sxs-lookup"><span data-stu-id="edfd3-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="edfd3-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="edfd3-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="edfd3-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="edfd3-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="edfd3-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="edfd3-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="edfd3-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="edfd3-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="edfd3-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="edfd3-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="edfd3-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="edfd3-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="edfd3-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="edfd3-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="edfd3-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="edfd3-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="edfd3-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="edfd3-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="edfd3-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="edfd3-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="edfd3-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="edfd3-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="edfd3-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="edfd3-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="edfd3-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="edfd3-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="edfd3-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="edfd3-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="edfd3-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="edfd3-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="edfd3-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="edfd3-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="edfd3-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="edfd3-223">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="edfd3-223">Added the following enhancements.</span></span>

* <span data-ttu-id="edfd3-224">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="edfd3-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="edfd3-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="edfd3-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="edfd3-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="edfd3-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="edfd3-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="edfd3-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="edfd3-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="edfd3-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="edfd3-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="edfd3-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="edfd3-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="edfd3-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="edfd3-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="edfd3-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="edfd3-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="edfd3-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="edfd3-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="edfd3-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="edfd3-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="edfd3-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="edfd3-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="edfd3-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="edfd3-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="edfd3-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="edfd3-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="edfd3-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="edfd3-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="edfd3-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="edfd3-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="edfd3-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="edfd3-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="edfd3-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="edfd3-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="edfd3-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="edfd3-250">**DML_OPERATOR_TOP_K** et **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="edfd3-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="edfd3-252">**DML_OPERATOR_REDUCE**, lors de l’utilisation de l’une des fonctions de réduction suivantes.</span><span class="sxs-lookup"><span data-stu-id="edfd3-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="edfd3-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="edfd3-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="edfd3-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="edfd3-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="edfd3-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="edfd3-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="edfd3-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="edfd3-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="edfd3-259">Restrictions de forme de tenseur souple pour **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="edfd3-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="edfd3-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="edfd3-261">Introduit dans DirectML version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="edfd3-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="edfd3-262">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="edfd3-262">Added the following APIs.</span></span>
* [<span data-ttu-id="edfd3-263">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="edfd3-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="edfd3-264">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="edfd3-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="edfd3-265">Requêtes au niveau des fonctionnalités (voir [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="edfd3-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="edfd3-266">Ajout de la prise en charge des types d’opérateurs suivants, documentés dans [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="edfd3-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="edfd3-267">Pour chaque constante de type d’opérateur, cette rubrique fournit un lien vers la structure correspondante.</span><span class="sxs-lookup"><span data-stu-id="edfd3-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="edfd3-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="edfd3-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="edfd3-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="edfd3-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="edfd3-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="edfd3-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="edfd3-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="edfd3-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="edfd3-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="edfd3-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="edfd3-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="edfd3-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="edfd3-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="edfd3-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="edfd3-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="edfd3-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="edfd3-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="edfd3-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="edfd3-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="edfd3-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="edfd3-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="edfd3-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="edfd3-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="edfd3-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="edfd3-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="edfd3-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="edfd3-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="edfd3-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="edfd3-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="edfd3-287">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="edfd3-287">Added the following enhancements.</span></span>

* <span data-ttu-id="edfd3-288">Lors de la liaison d’une ressource d’entrée pour la distribution d’un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), il est maintenant légal de fournir une ressource avec [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (en plus de **D3D12_HEAP_TYPE_DEFAULT**), à condition que les propriétés de tas appropriées soient également définies.</span><span class="sxs-lookup"><span data-stu-id="edfd3-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="edfd3-289">Consultez [liaison dans DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="edfd3-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="edfd3-290">Les opérateurs booléens logiques suivants prennent désormais en charge les dizaines de temps de sortie **UINT8** , en plus de la prise en charge existante de **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="edfd3-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="edfd3-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="edfd3-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="edfd3-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="edfd3-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="edfd3-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="edfd3-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="edfd3-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="edfd3-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="edfd3-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="edfd3-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="edfd3-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="edfd3-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="edfd3-298">5J les fonctions d’activation prennent désormais en charge l’utilisation de Strides sur leurs dizaines d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="edfd3-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="edfd3-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="edfd3-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="edfd3-300">Niveau de fonctionnalité dans lequel DirectML a été introduit.</span><span class="sxs-lookup"><span data-stu-id="edfd3-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="edfd3-301">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edfd3-301">See also</span></span>

* [<span data-ttu-id="edfd3-302">Historique des versions DirectML</span><span class="sxs-lookup"><span data-stu-id="edfd3-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="edfd3-303">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="edfd3-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="edfd3-304">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="edfd3-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="edfd3-305">Structure DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="edfd3-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
